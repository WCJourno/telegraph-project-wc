<script lang="ts">
  import rawBlocks from '$lib/doc.blocks.json';
  import DocRenderer from '$lib/components/DocRenderer.svelte';
  import type { Block } from '$lib/components/DocRenderer.svelte';
  const blocks = rawBlocks as Block[];
  import { base } from '$app/paths';
</script>

<!-- hard-coded custom code that should appear BEFORE Google Doc import can go here. -->

<main>

<!-- Section 1A: Hero page -->
<section class="hero-section">
    <div class="light-hero-box">
        <h1 class="text-center">THE AVE</h1>
        <h3 class="text-center">An interactive journey into the history of Berkeley’s student thoroughfare.</h3>
        <p> Standing on the corner of Telegraph Avenue and Bancroft Way, it’s easy to get caught up in the moment. Throngs of busy undergrads walk to and fro while student clubs and political candidates vie for the attention of passersby…</p>
    </div>
</section>

<!-- Section 1B: Text lede/historic scene setting/nut graf-->

<!-- Code imported from Google Doc -->

<section>
<div class="container">
  <div class="row justify-content-center">
    <div class="col-12 col-sm-10 col-lg-8 col-xxl-6">
      <DocRenderer {blocks} />
    </div>
  </div>
</div>
</section>

<!-- hard-coded custom code that should appear AFTER Google Doc import can go here. -->


<!-- DISABLING THIS SECTION 
<section class="dark-blue-tint-background">

    <div class="small-text-box">    
        <p>   ... the noise of the present often obscures the rich history of the place.</p>
    </div>

    <div class="small-text-box">    
        <p> Telegraph Avenue has been around for centuries. A north-south artery of the East Bay, it stretches TK miles, all the way to Oakland. At the north end, it once came all the way to Sather Gate–though it retreated to the corner of Bancroft Way in TK YEAR.</p>
    </div>

    <div class="small-text-box">    
        <p>… In the early 19th century, horse carriages rambled up and down the avenue, carrying students, professors and everyone else where they needed to go.</p>
    </div>

    <div class="small-text-box">    
        <p> … In the mid-20th century pictures of Telegraph Avenue were seen around the world, as the street acted as one of the iconic backdrops for a social movement…</p>
    </div>

    <div class="small-text-box">    
        <p> … and disastrous clashes between protesters and local, state and federal authorities.</p>
    </div>

    <div class="small-text-box">    
        <p> The businesses and buildings lining Telegraph Avenue have fluctuated as well. This project dives into some of the aspects that make this street unique such as street vendors and the city’s infamous history and its decline in bookstores, and highlights some of the street’s longest standing residents. Due to space and time constraints, this project will focus on the top five blocks of Telegraph Avenue, a favorite haunt of Berkeley students and the location of so many historic moments. </p>
    </div>

</section>
-->

<div class="story-background-photo">

<!-- Section 2: Street Vendors-->
<section class="red-tint-background">
    <div class="two-column-layout">
        <div class="box">
            <img src="{base}/images/jaffar-01-sm-static.png" alt="A longtime street vendor." style="width: 100%; height: auto;">
        </div>

        <div class="box">
            <h1> Heading</h1>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Cras tincidunt fringilla molestie. In mattis neque et enim eleifend malesuada. In non ex quam. Maecenas lorem metus, pharetra a odio in, molestie fermentum lectus. Proin non ultrices mauris, quis egestas est. Praesent purus felis, vehicula eget lacus ut, maximus ultricies est. Donec sit amet nibh ut leo volutpat vehicula ut id lectus. Phasellus suscipit risus ante, a volutpat massa gravida in. Vivamus aliquam, ex eget sollicitudin dictum, eros sem dapibus dui, id volutpat dolor sapien vel justo. Praesent auctor sem vitae nulla iaculis, non congue neque dictum. Nulla eleifend ut eros ut euismod. Praesent nec blandit lectus. Suspendisse a lectus quam. </p>
        </div>
    </div>
</section>

<!-- Section 3: Store Changes/Haste Intersection -->

<section class="yellow-tint-background">

    <div class="two-column-layout">
        <div class="color-1 box">
            <h1> This is some test text. How does this column look to you?</h1>
        </div>

        <div class="color-2 box">
            <h1> This is some test text. How does this column look to you?</h1>
        </div>
    </div>

</section>

<!-- Section 4: Bookstores -->
<section class="dark-blue-tint-background">

    <div class="two-column-layout">
        <div class="color-1 box">
            <img src="{base}/images/Moes-illustration.png" alt="Moe's Bookstore." style="width: auto; height: 600px;">
        </div>

        <div class="color-2 box">
            <h1> This is some test text. How does this second column look to you?</h1>
        </div>
    </div>

</section>

    <div class="carousel-box">
        <h1 class="text-center">Bookstores</h1>
        <h3 class=text-center>Flip through the history of bookstores in the Southside</h3>

        <div id="myCarousel" class="carousel slide">

        <!-- Indicators --> <!-- Carousel instructions: https://www.w3schools.com/bootstrap/bootstrap_carousel.asp -->
        <ol class="carousel-indicators">
            <li data-bs-target="#myCarousel" data-bs-slide-to="0" class="active"></li>
            <li data-bs-target="#myCarousel" data-bs-slide-to="1"></li>
            <li data-bs-target="#myCarousel" data-bs-slide-to="2"></li>
        </ol>

        <!-- Wrapper for slides -->
        <div class="carousel-inner">
            <div class="carousel-item active">
                <div class="carousel-caption">
                    <h3>Slide 01</h3>
                    <p>This is the first slide.</p>
                </div>
            <img src="/images/jaffar-01-sm-static.png" alt="Jaffar" class="d-block w-100">
            </div>

            <div class="carousel-item">
                <div class="carousel-caption">
                    <h3>Slide 02</h3>
                    <p>This is the second slide.</p>
                </div>
            <img src="/images/young-02-sm-static.png" alt="Young" class="d-block w-100">
            </div>

            <div class="carousel-item">

                <div class="carousel-caption">
                    <h3>Slide 03</h3>
                    <p>This is the third slide.</p>
                </div>
            <img src="/images/jaffar-01-sm-static.png" alt="Jaffar" class="d-block w-100">
            </div>
        </div>

        <!-- Left and right controls -->
        <button class="carousel-control-prev" type="button" data-bs-target="#myCarousel" data-bs-slide="prev">
            <span class="carousel-control-prev-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Previous</span>
        </button>
        <button class="carousel-control-next" type="button" data-bs-target="#myCarousel" data-bs-slide="next">
            <span class="carousel-control-next-icon" aria-hidden="true"></span>
            <span class="visually-hidden">Next</span>
        </button>
        </div>

    </div>

<!-- Section 5: Young's-->
<section class="yellow-tint-background">

    <div class="two-column-layout">
        <div class="color-1 box">
            <img src="{base}/images/young-02-sm-static.png" alt="Young himself." style="width: 100%; height: auto;">
        </div>

        <div class="color-2 box">
            <img src="{base}/images/2411telegraphstatic.png" alt="A building." style="width: 100%; height: auto;">
        </div>
    </div>

</section>

<!-- Section 6: Lunaparra/Future -->
<section class="dark-blue-tint-background">
    <div class="centered-text-box box">
        <h1 class="text-center">Another Section</h1>
        <h3 class=text-center>I'm trying a centered text box here.</h3>
    </div>

        <div class="two-column-layout">
            <div class="color-1 box">
                <h1> This is some test text. How does this second column look to you?</h1>
            </div>


            <div class="color-2 box">
                <h1> This is some test text. How does this second column look to you?</h1>
            </div>
        </div>

    <div class="two-column-layout">
        <div class="color-1 box">
            <img src="{base}/images/young-02-sm-static.png" alt="Young himself." style="width: 100%; height: auto;">
        </div>

        <div class="color-2 box">
            <h1> This is some test text. How does this column look to you?</h1>
        </div>
    </div>
</section>

</div>

</main>

<style lang="scss">

  .dark-blue-tint-background {
    background-color: rgba(0, 0, 139, 0.2); /* Dark blue tint */
    padding: 50px 20px; /* Add some padding for spacing */
  }

  .red-tint-background {
    background-color: rgba(255, 0, 0, 0.2); /* Red tint */
    padding: 50px 20px; /* Add some padding for spacing */
  }

  .yellow-tint-background {
    background-color: rgba(250, 239, 140, 0.2); /* Yellow tint */
    padding: 50px 20px; /* Add some padding for spacing */
  }

</style>