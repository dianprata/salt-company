<script setup lang="ts">
function scrollTo(id: string) {
  const element = document.getElementById(id)
  element?.scrollIntoView({ behavior: 'smooth' })
}

const openNavbar = ref(false)
</script>

<template>
  <div class="relative flex items-center justify-between gap-2 bg-white px-8 py-3">
    <NuxtLink>
      <Logo />
    </NuxtLink>
    <div class="hidden items-center gap-6 md:flex">
      <div class="cursor-pointer" @click="scrollTo('slider')">
        Who We Are
      </div>
      <div class="cursor-pointer" @click="scrollTo('our-values')">
        Our Values
      </div>
      <div class="cursor-pointer" @click="scrollTo('our-speciality')">
        The Perks
      </div>
    </div>
    <IconBurger v-if="!openNavbar" class="md:hidden" @click="openNavbar = true" />
    <div v-else class="i-carbon-close text-xl md:hidden" @click="openNavbar = false" />
    <div v-if="openNavbar" class="absolute left-0 top-[56px] z-100 w-full flex flex-col bg-white md:hidden">
      <div class="cursor-pointer px-6 py-3" @click="scrollTo('slider')">
        Who We Are
      </div>
      <div class="cursor-pointer px-6 py-3" @click="scrollTo('our-values')">
        Our Values
      </div>
      <div class="cursor-pointer px-6 py-3" @click="scrollTo('our-speciality')">
        The Perks
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
