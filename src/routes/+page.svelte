<script>
  import { onMount } from "svelte";

  let currentSlide = 1;
  let slideCount = 3; // We have slides from 1 to 3

  onMount(() => {
    const interval = setInterval(() => {
      currentSlide = currentSlide % slideCount + 1;
    }, 3000); // Change slide every 3 seconds

    return () => clearInterval(interval); // Clear interval on component destroy
  });
</script>

<div
  class="hero min-h-screen"
  style="background-image: url(https://source.unsplash.com/featured/?computers);"
>
  <div class="hero-overlay bg-opacity-60" />
  <div class="hero-content text-center text-neutral-content">
    <div class="max-w-md">
      <h1 class="mb-5 text-5xl font-bold ">Hello there</h1>
      <p class="mb-5">What Technological Issues are you Facing today?!</p>
      <button class="btn btn-primary">Get Started</button>
    </div>
  </div>
</div>

<!-- Carousel Section -->
<div class="carousel w-full">
  <div class:active={currentSlide === 1} class="carousel-item relative w-full">
    <img src="https://source.unsplash.com/featured/?computer-screen" class="w-full" />
    <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
      <!-- <a href="#slide3" class="btn btn-circle">❮</a> 
      <a href="#slide2" class="btn btn-circle">❯</a> -->
    </div>
  </div> 

  <div class:active={currentSlide === 2} class="carousel-item relative w-full">
    <img src="https://source.unsplash.com/featured/?computer-keyboards" class="w-full" />
    <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
      <!-- <a href="#slide1" class="btn btn-circle">❮</a> 
      <a href="#slide3" class="btn btn-circle">❯</a> -->
    </div>
  </div> 

  <div class:active={currentSlide === 3} class="carousel-item relative w-full">
    <img src="https://source.unsplash.com/featured/?computer-mouse" class="w-full" />
    <div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-1/2">
      <!-- <a href="#slide2" class="btn btn-circle">❮</a> 
      <a href="#slide1" class="btn btn-circle">❯</a> -->
    </div>
  </div> 
</div>


<div class="text-center justify-center ">
  <h1 class="font-bold text-4xl text-white drop-shadow-2xl w-max mx-auto">What I am About</h1>
  <div class="collapse collapse-arrow bg-base-200">
    <input type="radio" name="my-accordion-2" checked="checked" />
    <div class="collapse-title text-xl font-medium">
      General Technological Issues
    </div>
    <div class="collapse-content">
      <p>
        General issues like printer issues, or network connectivity issues.
      </p>
    </div>
  </div>
  <div class="collapse collapse-arrow bg-base-200">
    <input type="radio" name="my-accordion-2" />
    <div class="collapse-title text-xl font-medium">
      Full-Stack Web Development
    </div>
    <div class="collapse-content">
      <p>
        I need to write stuffs about web development and how I build full-stack
        websites.
      </p>
    </div>
  </div>
  <div class="collapse collapse-arrow bg-base-200">
    <input type="radio" name="my-accordion-2" />
    <div class="collapse-title text-xl font-medium">Web Design</div>
    <div class="collapse-content">
      <p>
        Write about how I turn concepts into design for their business needs.
      </p>
    </div>
  </div>
  <div class="collapse collapse-arrow bg-base-200">
    <input type="radio" name="my-accordion-2" />
    <div class="collapse-title text-xl font-medium">
      Database & Authentication
    </div>
    <div class="collapse-content">
      <p>
        Talk about how I can implement database infrastructure for their
        business. How can I also implement proper authorization and
        authentication for their business needs.
      </p>
    </div>
  </div>
</div>


<style>
  .carousel-item {
    display: none;
  }
  .carousel-item.active {
    display: block;
  }
</style>

