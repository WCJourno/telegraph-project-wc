<script lang="ts">
  import rawBlocks from '$lib/doc.blocks.json';
  import DocRenderer from '$lib/components/DocRenderer.svelte';
  import type { Block } from '$lib/components/DocRenderer.svelte';
  const blocks = rawBlocks as Block[];
  import { base } from '$app/paths';
</script>


<!-- hard-coded custom code that should appear BEFORE Google Doc import can go here. -->

<main>

<!-- Header/Intro -->
<div class="hero-section">
    <h1 class="text-center">Welcome to Telegraph Avenue</h1>
    <h3 class="text-center">Our project will take readers on a tour of this historic neighborhood.</h3>
    <p class="text-center"> We'll have a brief introduction here followed by a scrolling illustrated map. Which will introduce readers to notable characters along the street.</p>
</div>


<div class="story-background-photo">
<!-- Section 1a: Street Vendors, Column 1 -->
<div class="two-column-layout">
    <div class="color-1 box">
        <img src="{base}/images/jaffar-01-sm-static.png" alt="A longtime street vendor." style="width: 100%; height: auto;">
    </div>

<!-- Section 1b: Street Vendors, Column 2 -->
    <div class="color-2 box">
        <h1> This is some test text. How does this second column look to you?</h1>
    </div>
</div>

<!-- Section 2a: 2411 Telegraph Avenue, Column 1 -->
<div class="two-column-layout">
    <div class="color-1 box">
        <h1> This is some test text. How does this column look to you?</h1>
    </div>

<!-- Section 2b: 2411 Telegraph Avenue, Column 2 -->
	<div class="color-2 box">
		<h1> This is some test text. How does this column look to you?</h1>
	</div>
</div>

<!-- Section 3: Bookstores, Centered text box -->

  <div class="centered-text-box box">
	<h1 class="text-center">Bookstores</h1>
	<h3 class=text-center>I'm trying a centered text box here.</h3>
  </div>


<!-- Section 4a: Bookstores, Column 1 -->
<div class="two-column-layout">
    <div class="color-1 box">
		<img src="{base}/images/Moes-illustration.png" alt="Moe's Bookstore." style="width: 100%; height: auto;">
	</div>

<!-- Section 4b: Bookstores, Column 2 -->
    <div class="color-2 box">
        <h1> This is some test text. How does this second column look to you?</h1>
    </div>
</div>

<!-- Section 5a: Young's, Column 1 -->
<div class="two-column-layout">
    <div class="color-1 box">
        <h1> This is some test text. How does this column look to you?</h1>
    </div>

<!-- Section 5b: Young's, Column 2 -->
    <div class="color-2 box">
        <img src="{base}/images/2411telegraphstatic.png" alt="A building." style="width: 100%; height: auto;">
    </div>
</div>

<!-- Section 6: Centered text section -->
  <div class="centered-text-box box">
	<h1 class="text-center">Another Section</h1>
	<h3 class=text-center>I'm trying a centered text box here.</h3>
  </div>


<!-- Section 7a: Bookstores, Column 1 -->
<div class="two-column-layout">
    <div class="color-1 box">
        <h1> This is some test text. How does this second column look to you?</h1>
    </div>

<!-- Section 7b: Bookstores, Column 2 -->
    <div class="color-2 box">
        <h1> This is some test text. How does this second column look to you?</h1>
    </div>
</div>

<!-- Section 8a: Young's, Column 1 -->
<div class="two-column-layout">
    <div class="color-1 box">
		 <img src="{base}/images/young-02-sm-static.png" alt="Young himself." style="width: 100%; height: auto;">
    </div>

<!-- Section 8b: Young's, Column 2 -->
    <div class="color-2 box">
        <h1> This is some test text. How does this column look to you?</h1>
    </div>

</div>
</div>

<!-- Code imported from Google Doc -->

<!-- I'm disabling this section for now.
<div class="container">
  <div class="row justify-content-center">
    <div class="col-12 col-sm-10 col-lg-8 col-xxl-6">
      <DocRenderer {blocks} />
    </div>
  </div>
</div>
End disabled section -->

<!-- hard-coded custom code that should appear AFTER Google Doc import can go here. -->

</main>