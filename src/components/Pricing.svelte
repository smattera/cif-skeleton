<div class="hero px-4 md:px-0">
  <h2 class="font-bold mb-4 text-center">Ticket Presale Starts On Monday, June 12, 2023</h2>
  <div class="flex flex-col lg:flex-row justify-center items-center w-full h-full text-center">
    <div class="bg-child rounded-md shadow-lg p-6 m-4 w-full h-full outline outline-white outline-offset-4">
      <h2 class="text-5xl font-bold" style="text-shadow:5px 5px 10px #333">Child Pass</h2>
			<div class="outline outline-neutral rounded-lg mx-auto p-2 m-4 text-3xl" style="text-shadow:4px 4px 6px #333;box-shadow: 5px 5px 10px #333;">AGES 5 & UNDER</div>
			<h2 class="text-9xl font-bold py-10" style="text-shadow:5px 5px 10px #333;font-size:5rem;">FREE</h2>
    </div>
    <div class="bg-student rounded-md shadow-lg p-6 m-4 w-full h-full outline outline-white outline-offset-4">
      <h2 class="text-5xl font-bold" style="text-shadow:5px 5px 10px #333">Student Pass</h2>
			<div class="outline outline-neutral rounded-lg mx-auto p-2 m-4 text-3xl" style="text-shadow:4px 4px 6px #333;box-shadow: 5px 5px 10px #333;">AGES 6 - 17</div>
			<h2 class="text-5xl font-bold" style="text-shadow:5px 5px 10px #333">Season $10</h2>
			<hr class="rounded-lg my-4" style="border: 3px solid #fff;box-shadow: 3px 3px 6px #333"/>
			<h2 class="text-5xl font-bold" style="text-shadow:5px 5px 10px #333">Day $7</h2>
    </div>
    <div class="bg-adult rounded-md shadow-lg p-6 m-4 w-full h-full outline outline-white outline-offset-4">
      <h2 class="text-5xl font-bold" style="text-shadow:5px 5px 10px #333">Adult Pass</h2>
			<div class="outline outline-neutral rounded-lg mx-auto p-2 m-4 text-3xl" style="text-shadow:4px 4px 6px #333;box-shadow: 5px 5px 10px #333;">AGES 18 & OVER</div>
			<h2 class="text-5xl font-bold" style="text-shadow:5px 5px 10px #333">Season $20</h2>
			<hr class="rounded-lg my-4" style="border: 3px solid #fff;box-shadow: 3px 3px 6px #333"/>
			<h2 class="text-5xl font-bold" style="text-shadow:5px 5px 10px #333">Day $12</h2>
    </div>
  </div>
</div>

<style>
  .hero {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding-top: 30px;
    padding-bottom: 30px;
    background: url("/weave02.svg") center repeat-x,
    #212529;
    background-blend-mode: lighten;
  }
  .hero h2 {
    text-shadow: 0px 0px 8px #aaa;
  }
  .hero div div h2 {
    font-size: clamp(2rem, 5vw, 3rem);
		font-weight: 600;
  }
  .hero div div div {
    font-size: clamp(1rem, 5vw, 2rem);
  }
  .bg-child {
		background: linear-gradient(midnightblue, purple, lightpink);
	}
	.bg-student {
		background: linear-gradient(darkolivegreen, green, lightgreen);
	}
	.bg-adult {
		background: linear-gradient(maroon, red, orange);
	}
</style>
