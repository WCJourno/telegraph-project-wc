<script lang="ts">
  import rawBlocks from '$lib/doc.blocks.json';
  import DocRenderer from '$lib/components/DocRenderer.svelte';
  import type { Block } from '$lib/components/DocRenderer.svelte';
  const blocks = rawBlocks as Block[];
</script>


<!-- hard-coded custom code that should appear BEFORE Google Doc import can go here. -->

<main>


  <div class="container">
    <h1 class="text-center">Welcome to Telegraph Avenue</h1>
    <h3 class="text-center">This is a tour of a historic neighborhood.</h3>
  </div>

  <div class="container telegraph-map">
  </div>

  <div class="container">
    <h1 class="text-center">Street Vendors</h1>
    <p> We'll have a video interview with a longtime street vendor here.</p>
    <img src="src/lib/assets/jaffar-01.png" alt="Image of Jaffar" class="img-fluid"/>
  </div>

  <div class="container">
    <h1 class="text-center">Bookstores</h1>
    <p> Telegraph Avenue was once home to over a dozen bookstores. Now, only two remain.</p>
    <iframe src="https://www.google.com/maps/d/u/0/embed?mid=1ZQE6JvlZcT-HLbFwUMsUxFjQmuUqQtE&ehbc=2E312F&noprof=1" width="640" height="480"></iframe>
  </div>

  <div class="container">
    <h1 class="text-center">Young's Backpacking</h1>
    <p> This store has been on Telegraph Avenue for 40 years.</p>
    <img src="src/lib/assets/young-02.png" alt="Image of Youngs owner" class="img-fluid"/>
  </div>

    <div class="container">
    <h1 class="text-center">2411 Telegraph Avenue</h1>
    <p> Despite changes on Telegraph Avenue, many buildings have remained relatively unchanged despite housing many businesses over the years.</p>
    <!-- svelte-ignore a11y_img_redundant_alt -->
    <img src="src/lib/assets/2411telegraph.jpg" alt="Image of 2411 Telegraph Avenue" class="img-fluid"/>
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