<script lang="ts">
	import Countdown from "../components/Countdown.svelte";

  let videos = [
    "vid/Promo.mp4",
    "vid/CIFVideoWeb02.mp4",
    "vid/CIFVideoWeb03.mp4",
  ];
  let currentVideo = 0;

  function nextVideo() {
    currentVideo = (currentVideo + 1) % videos.length;
    (document.getElementById("bgvid") as HTMLVideoElement).src = videos[currentVideo];
  }
</script>

<svelte:head>
	<title>Choctaw Indian Fair | Home</title>
</svelte:head>

<video autoplay muted loop playsinline id="bgvid" on:ended={nextVideo} class="relative top-0 left-0 w-full object-cover -z-[1] h-[75vh]">
  <source src="{videos[0]}" type="video/mp4">
</video>

<!-- <video autoplay loop muted playsinline class="relative top-0 left-0 w-full object-cover -z-[1] h-[75vh]" poster="./img/CIF-bg.webp">
	<source src="./vid/CIFVideoWeb.mp4" type="video/mp4"/>
</video> -->

<Countdown />

<section class="flex flex-col md:flex-row items-center py-12 px-4">
  <div class="md:w-1/2 md:pr-8 max-w-5xl mx-auto">
    <img src="/img/chiefprincess.webp" alt="Chief & Princess" class="rounded-lg shadow-lg"/>
  </div>
  <div class="md:w-1/2 text-center pt-10 md:pt-0">
		<h1><span class="gradient-heading">Halito!</span></h1>
    <p class="my-2">
      Greetings from the Choctaw Indian Reservation. We invite you to join us July 12-15 for our 73rd annual Choctaw Indian Fair. The fair takes place on our centuries-old homeland in beautiful Choctaw, Mississippi. We gather each July to celebrate our heritage and share our beautiful and vibrant culture with our friends and neighbors. This year's fair theme is:
    </p>
    <h2 class="py-2">"The Choctaw Spirit Lives On"</h2>
    <p class="my-2">
      Fairgoers will experience the magnificent journey of our people through historical and cultural displays, social dancing, tribal arts & crafts, Choctaw stickball - the granddaddy of all field sports - as well as the Choctaw Indian Princess Pageant and traditional Choctaw food. The fair also offers carnival rides and games for the young and old alike, Shawi's Discovery Zone and chart-topping musical acts each night. There's something for everyone at the Choctaw Indian Fair - we'll see you soon!
    </p>
    <h1><span class="gradient-heading">Yakoki!</span></h1>
  </div>
</section>

<style>
	section {
    background: center / cover url('/isometric.svg'), linear-gradient(to bottom right, red, maroon);
		background-blend-mode: darken;
  }
	h1 .gradient-heading {
    font-size: clamp(3rem, 5vw, 6rem);
		font-weight: 600;
		@apply bg-clip-text text-transparent box-decoration-clone;
		/* Direction */
		@apply bg-gradient-to-br;
		/* Color Stops */
		@apply from-primary-500 via-surface-50 to-primary-600;
	}
  h2 {
		font-size: clamp(1rem, 5vw, 3rem);
		font-weight: 600;
	}
  p {
    font-size: clamp(1rem, 1.25vw, 1.5rem);
  }
</style>
