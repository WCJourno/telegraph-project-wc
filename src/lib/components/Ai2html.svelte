<script>
  import { onMount, tick } from 'svelte';

  export let slug = ''; // slug is named of ai file
  export let imagePath = '/ai2html/';
  export let imgPathPlaceholder = 'IMG_PATH';

  export let fullWidth = true // change to false in the gdoc if you want the graphic to be contained to container

  let htmlContent = '';
  let error = null;
  let container;

  // Only used in fullWidth mode: swap @container → @media
  function containerQueriesToMediaQueries(html) {
    return html.replace(
      /@container\s+[\w-]+\s*\(([^)]+)\)(?:\s+and\s+\(([^)]+)\))?/g,
      (_, first, second) => {
        const convert = (c) =>
          c
            .replace(/width\s*>=\s*(\d+)px/, 'min-width: $1px')
            .replace(/width\s*>\s*(\d+)px/, (_, n) => `min-width: ${+n + 1}px`)
            .replace(/width\s*<=\s*(\d+)px/, 'max-width: $1px')
            .replace(/width\s*<\s*(\d+)px/, (_, n) => `max-width: ${+n - 1}px`);
        const parts = [convert(first)];
        if (second) parts.push(convert(second));
        return `@media (${parts.join(') and (')})`;
      }
    );
  }

  // Fix fluid scaling for fixed-size artboards (fit / large)
  function fixArtboardScaling(root) {
    root.querySelectorAll('.g-artboard, .dvz-artboard').forEach((board) => {
      const ratio = parseFloat(board.getAttribute('data-aspect-ratio'));
      if (!ratio) return;
      const spacer = board.querySelector(':scope > div:first-child');
      const hasPaddingTrick = spacer && spacer.style.paddingBottom;
      if (!hasPaddingTrick) {
        board.style.width = '100%';
        board.style.maxWidth = '100%';
        board.style.height = 'auto';
        if (spacer) {
          spacer.style.paddingBottom = `${(1 / ratio) * 100}%`;
          spacer.style.position = 'relative';
        }
      } else {
        board.style.width = '100%';
      }
    });
  }

  async function loadHtml(s) {
    if (!s) return;
    error = null;
    htmlContent = '';
    try {
      const url = `${imagePath}${s}.ai2html.html`;
      const res = await fetch(url);
      if (!res.ok) throw new Error(`Could not load ${url} (HTTP ${res.status})`);

      let raw = await res.text();
      raw = raw.replaceAll(imgPathPlaceholder, imagePath.replace(/\/$/, ''));
      if (fullWidth) raw = containerQueriesToMediaQueries(raw);

      htmlContent = raw;
      await tick();
      if (container) fixArtboardScaling(container);
    } catch (e) {
      error = e.message;
    }
  }

  onMount(() => loadHtml(slug));
  $: if (slug) loadHtml(slug);
</script>

{#if htmlContent}
  <div
    class="ai2html-outer"
    class:ai2html-breakout={fullWidth}
    bind:this={container}
  >
    {@html htmlContent}
  </div>
{/if}

<style>
  .ai2html-outer {
    width: 100%;
  }

  /* Full-bleed breakout — only applied when fullWidth=true */
  .ai2html-breakout {
    width: 100vw;
    position: relative;
    left: 50%;
    transform: translateX(-50%);
  }

  .ai2html-loading {
    min-height: 4rem;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .ai2html-placeholder { color: #888; font-size: 0.9rem; margin: 0; }

  .ai2html-outer :global(.g-artboard),
  .ai2html-outer :global(.dvz-artboard) {
    position: relative;
  }
</style>