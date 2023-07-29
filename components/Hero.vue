<script setup lang="ts">
import ScrollToBottom from '~/components/icon/ScrollToBottom.vue'

function scrollToSlider() {
  const slider = document.getElementById('slider')
  slider?.scrollIntoView({ behavior: 'smooth' })
}
</script>

<template>
  <div class="relative">
    <img src="/bg-hero.svg" alt="" class="relative aspect-2/1 h-full w-full object-cover">
    <HeroCoverBack class="absolute right-0 z-1 h-auto w-full -mt-18 md:hidden" />
    <HeroCoverFront class="absolute left-0 z-10 h-auto w-full -mt-20 md:hidden" />
    <div class="relative z-50 my-10 px-10 text-white md:absolute md:top-1/3 md:mt-0 sm:mb-24 sm:mt-20 md:bg-black/50 md:p-10">
      <h1 class="mb-4 text-4xl font-medium">
        Discover <br> Your Wonder
      </h1>
      <p>
        Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam.
      </p>
    </div>
    <ScrollToBottom class="relative z-100 mx-auto cursor-pointer -mt-6" @click="scrollToSlider" />
  </div>
</template>

<style scoped>
</style>
