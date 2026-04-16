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
<div class="container" style="background-color: rgba(240, 240, 240, 0.8); border-radius: 10px; padding: 2rem; margin-bottom: 2rem;">
    <h1 class="text-center">Welcome to Telegraph Avenue</h1>
    <h3 class="text-center">Our project will take readers on a tour of this historic neighborhood.</h3>
    <p> We'll have a brief introduction here followed by a scrolling illustrated map. Which will introduce readers to notable characters along the street.</p>
</div>


<!-- Section 1: Street Vendors, Column 1 -->
<div class="two-column-layout">
    <div>
        <img src="{base}/images/jaffar-01-sm-static.png" alt="A longtime street vendor." style="width: 100%; height: auto;">
    </div>

<!-- Section 1: Street Vendors, Column 2 -->
    <div>
        <h1> This is some test text. How does this second column look to you?</h1>
    </div>
</div>

<!-- Section 2: 2411 Telegraph Avenue, Column 1 -->
<div class="two-column-layout">
    <div>
        <h1> This is some test text. How does this column look to you?</h1>
    </div>

<!-- Section 2: 2411 Telegraph Avenue, Column 2 -->
    <div>
    </div>
</div>

<!-- Section 3: Bookstores, Column 1 -->
<div> 
  <h1 class="text-center" style="color: blue; background-color: tan;"> Bookstores </h1>
<div class="two-column-layout">
    <div>
        <iframe src="https://www.google.com/maps/d/u/0/embed?mid=1ZQE6JvlZcT-HLbFwUMsUxFjQmuUqQtE&ehbc=2E312F&noprof=1" width="100%" height="100%"></iframe>
    </div>

<!-- Section 3: Bookstores, Column 2 -->
    <div>
        <h1> This is some test text. How does this second column look to you?</h1>
    </div>
</div>
</div>

<!-- Section 4: Young's, Column 1 -->
<div class="two-column-layout">
    <div>
        <h1> This is some test text. How does this column look to you?</h1>
    </div>

<!-- Section 4: Young's, Column 2 -->
    <div>
        <img src="{base}/images/young-02-sm-static.png" alt="Young himself." style="width: 100%; height: auto;">
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