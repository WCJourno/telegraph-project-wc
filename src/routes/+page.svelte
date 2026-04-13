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
  <div class="container">
    <h1 class="text-center">Welcome to Telegraph Avenue</h1>
    <h3 class="text-center">Our project will take readers on a tour of this historic neighborhood.</h3>
    <p> We'll have a brief introduction here followed by a scrolling illustrated map. Which will introduce readers to notable characters along the street.</p>
  </div>


<!-- Map 1: Street Vendors-->
<div
  class="container telegraph-map"
  style={`background-image: url('${base}/images/Map1_StreetVendor-800.png');`}
>
</div>

<!-- Section 1: Street Vendors -->
 <div class="container">
    <h1 class="text-center">Street Vendors</h1>
    <p> First, we'll have a video interview with a longtime street vendor here.</p>
    <img src="{base}/images/jaffar-01-sm-static.png" alt="Jaffar, a longtime street vendor on Telegraph Avenue, stands on the street in an urban setting. He appears friendly and approachable, representing the diverse vendor community that has been central to the neighborhood's character." class="img-fluid"/>
  </div>


  <!-- Map 2: Copy Central/2411 Telegraph Avenue -->

<div
  class="container telegraph-map"
  style={`background-image: url('${base}/images/Map2_CopyCentral-800.png');`}
>
</div>

  <!-- Section 2: Copy Central/2411 Telegraph Avenue -->

  <div class="container">
    <h1 class="text-center">2411 Telegraph Avenue</h1>
    <p> This section will have an animation highlighting the history of a building which has been home to many businesses over the past few decades.</p>
    <img src="{base}/images/2411telegraphstatic.png" alt="2411 Telegraph Avenue storefront" class="img-fluid"/>
  </div>

  <!-- Map 3: Bookstores -->

<div
  class="container telegraph-map"
  style={`background-image: url('${base}/images/Map3_MoesBooks-800.png');`}
>
</div>

  <!-- Section 3: Bookstores -->

  <div class="container">
    <h1 class="text-center">Bookstores</h1>
    <p> Telegraph Avenue was once home to over a dozen bookstores. Now, only two remain. This section will have an interactive feature allowing readers to explore the history.</p>
    <iframe src="https://www.google.com/maps/d/u/0/embed?mid=1ZQE6JvlZcT-HLbFwUMsUxFjQmuUqQtE&ehbc=2E312F&noprof=1" width="100%" height="480"></iframe>
  </div>

<!-- Map 4: Young's Backpacking -->

<div
  class="container telegraph-map"
  style={`background-image: url('${base}/images/Map4_Youngs-800.png');`}
>
</div>

<!-- Section 4: Young's Backpacking -->

  <div class="container">
    <h1 class="text-center">Young's Backpacking</h1>
    <p> This store has been on Telegraph Avenue for 40 years. We'll highlight the story using a video interview with the owner and photos.</p>
    <img src="{base}/images/young-02-sm-static.png" alt="Young himself" class="img-fluid"/>
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