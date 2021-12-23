<template>
  <div class="hero h-[30vh] sm:h-[50vh] px-9 sm:px-16 py-16 sm:py-32">
    <div class="">
      <h1
        class="w-full sm:w-[20rem] lg:w-[30rem] font-serif text-white text-2xl sm:text-4xl lg:text-6xl mb-5"
      >
        What it's like to travel to Hawaii right now
      </h1>

      <p
        class="w-fit text-lg sm:text-xl lg:text-2xl py-2 border-gray-400 border-t-2 text-white font-sans"
      >
        Free flights to remote workers
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HeroSection',
};
</script>

<style>
.hero {
  background-image: linear-gradient(
      90deg,
      rgba(0, 0, 0, 0.754359243697479) 0%,
      rgba(9, 9, 121, 0) 50%
    ),
    url('../assets/hawaii.jpg');
  background-repeat: no-repeat;
  background-size: cover;
  background-position: 25% 94%;
}
</style>
