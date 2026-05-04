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
<section class="hero-section red-tint-background">
    <video autoplay muted loop id="myVideo">
        <source src="{base}/videos/Tele-Bancroft-Video.mp4" type="video/mp4">
    </video>
    <div class="light-hero-box">
        <img src="{base}/images/WelcomeIllustration.png" alt="Welcome to Telegraph Avenue" style="width: 60vh; height: auto; margin:auto; display:block;">
        <p class="text-center"> An interactive tour by Will Carruthers, Hamza Adel Fahmy and Chloe Swedberg</p>
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

<!--- Section 1b: Welcome to Telegraph Avenue-->
<section class="bottom-margin"> 
    <div class="centered-telegraph-box box">
        <img src="{base}/images/TelegraphAveSign.png" alt="Sign." style="width: auto; height: 100%; margin:auto; display:block;">
    </div>
</section>

<!-- Section 2: Street Vendors-->
<section class="red-tint-background bottom-margin">
    <div class="two-column-layout">

        <div class="box">
            <h1> Street Vendors</h1>
            <p>Zaffar Mahmoud has been laying out his jewelry to sell on Telegraph Avenue since 1980, back when the street still felt like an open-air gallery. In those days, the sidewalks were filled with other vendors sharing handmade wares. That world hasn’t disappeared, but it’s gotten quieter. Over time, Zaffar says selling here has become less about craft and more about keeping up— faster products and shifts in taste have made fewer vendors willing or able to stay. </p>
            <p>Many have packed up, moved on, or changed what they make just to get by. Zaffar remains a constant on a street that rarely is, one where the value wasn’t just in what you bought, but in who you met along the way. </p>
        </div>

        <div class="box">
            <iframe width="500px" height="315px" src="https://www.youtube.com/embed/v0JEVTtJHzk?si=FwnqQAovZxTm4-ZA" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
        </div>
    </div>
</section>

<!-- Section 3: Store Changes/Haste Intersection -->

<section class="yellow-tint-background bottom-margin">

    <div class="two-column-layout">
        <div class="color-1 box">
            <h1>Store Changes</h1>
            <p>Though some buildings on Telegraph Avenue have been largely unchanged, serving a series of businesses over the decades, many other buildings have been torn down and replaced. Two buildings at the corner of Haste Street and Telegraph Avenue offer an example of this dichotomy. </p>
        </div>

        <div class=" color-2 box">
            <img src="{base}/images/CopyCentral-1000px.png" alt="2411 Telegraph Avenue." style="width: 100%; height: auto;">
            <p>At 2411 Telegraph Ave., a colorful marquee today advertises the offerings of the Copy Central inside. The same building has housed numerous businesses in the past, including Armadillo Pizza in the 1980s and, in the early 2000s, a branch of Rasputin Records specializing in videos. Decades earlier, as the building’s exterior suggests, 2411 Telegraph Ave. was the location of the Sunset Theater and then the D.K. Theater. Both went out of business, part of a greater trend of local theaters disappearing across Berkeley. </p>
        </div>
    </div>

    <div class="two-column-layout">
        <div class="color-1 box">
            <p> Right next door to 2411 Telegraph Ave. is 2503 Haste Street, a site of much civic consternation. The land was once covered by the Berkeley Inn, a 75-room hotel which was demolished in 1990 after suffering a series of fires. The property was an empty lot and eyesore for decades before it was finally replaced by a hulking student housing complex completed in 2020. The new building, dubbed the Enclave, was the subject of much discussion. Bland critics called it “funky” and “the ugliest building in Berkeley” while more creative ones painted an image with words. San Francisco Chronicle columnist John King wrote that the Enclave looks “as if Harry Potter and Fred Flintstone decided to build a McMansion. On acid."</p>
            <img src="{base}/images/Telegraph-Haste-1800px.png" alt="2503 Haste Street & Amoeba Music." style="width: 100%; height: auto;">
        </div>

         <div class="color-2 box"></div>
    </div>

</section>

<!-- Section 4: Bookstores -->
<section class="dark-blue-tint-background">

    <div class="two-column-layout">
        <div class="color-1 box">
            <img src="{base}/images/MoesBooks-1000px.png" alt="Moe's Bookstore." style="width: auto; height: 600px;">
        </div>

        <div class="color-2 box">
            <h1> Bookstores</h1>
            <p>Throughout the 20th century, Berkeley was home to dozens of bookstores. In 1986, a guidebook listed 45 independent bookstores throughout the city, with 15 clustered within a five-block section of the Southside. Bookstores appear in the background of many historic photos of the street–and, at other times, made news themselves. </p>
            <p> Click the arrow on the right to explore some of the historical highlights. </p>
        </div>
    </div>

</section>

    <div class="carousel-box bottom-margin">
        <!-- DISABLING CAROUSEL HEADER TEXT FOR NOW
        <h1 class="text-center">Bookstores</h1>
        <h3 class=text-center>Flip through the history of bookstores in the Southside</h3>
        -->

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
            <img src="{base}/images/jaffar-01-sm-static.png" alt="Jaffar" class="d-block w-100">
            </div>

            <div class="carousel-item">
                <div class="carousel-caption">
                    <h3>Slide 02</h3>
                    <p>This is the second slide.</p>
                </div>
            <img src="{base}/images/young-02-sm-static.png" alt="Young" class="d-block w-100">
            </div>

            <div class="carousel-item">

                <div class="carousel-caption">
                    <h3>Slide 03</h3>
                    <p>This is the third slide.</p>
                </div>
            <img src="{base}/images/jaffar-01-sm-static.png" alt="Jaffar" class="d-block w-100">
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
<section class="yellow-tint-background bottom-margin">

    <div class="two-column-layout">
        <div class="color-1 box">
            <h1 class="text-center">Young's Backpacking</h1>
            <p> Young’s Backpacks is one of Telegraph’s quieter anchors. Its story starts in 1983, when Min Young arrived in the United States as a young man who had served in the Korean army and developed a reputation as an accomplished mountaineer. Young built his small camping store piece by piece until it became something steady and familiar. </p>
            <p> Four decades later, Young is still on Telegraph Avenue, but the street around him has shifted. The independent, family-run shops that once defined the street are fading due to increasing rents and the rise of online retail. He points just next door to places like Hats of Berkeley — a longtime business which shuttered their doors earlier this year — as an example of what’s being lost. Young’s store remains, but like Zaffar on the sidewalk, it stands on a thinning landscape. </p>
        </div>

        <div class="color-2 box">
            <img src="{base}/images/YoungsBackpacking-01-1000px.png" alt="A building." style="width: 100%; height: auto;">
        </div>
    </div>

    <div class="centered-text-box box">
        <iframe width="800" height="500" src="https://www.youtube.com/embed/Q1xNUD7Zuvo?si=ArRCtVO0HRyKRQWw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen style="margin:auto; display:block;"></iframe>
    </div>

</section>

<!-- Section 6: Lunaparra/Future -->
<section class="dark-blue-tint-background bottom-margin">
     <div class="box">
        <h1 class="text-center">Councilmember Lunaparra ponders the future</h1>
    </div>
 
    <div class="two-column-layout">
        <div class="color-1 box">
             <p> Berkeley City Councilmember Cecilia Lunaparra looks at Telegraph Avenue for both what it is today, and what it could  become. While representing Berkeley’s Southside on the city council for the past two years, she has seen the same pattern playing out block by block: longtime mom-and-pop shops, especially retail stores, struggling to hold on, while a new wave of businesses—boba shops, quick-turn storefronts—move in to meet changing demand. </p>
            <p> For Lunaparra, the future of Telegraph isn’t just about what fills the storefronts, but about reimagining the street itself. She talks about the possibility of a car-free corridor– a Telegraph that shifts its focus back to pedestrians, vendors and students. It’s an idea that echoes the avenue’s past while pushing it forward: making it into an area less defined by lines of double-parked food delivery drivers and business closures, and more by community, where the rhythm of the street might once again be shaped by those who spend time on it. </p>
        </div>

        <div class="color-2 box">
            <img src="{base}/images/young-02-sm-static.png" alt="Young himself." style="width: 100%; height: auto;">
        </div>
    </div>

</section>

</div>

</main>
