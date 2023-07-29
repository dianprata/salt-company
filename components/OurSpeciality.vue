<script setup lang="ts">
import { ref } from 'vue'
import { IconAccesories, IconExhaust, IconSpeedImprovement } from '#components'

const items = [
  {
    id: 1,
    title: 'Exhaust',
    icon: IconExhaust,
  },
  {
    id: 2,
    title: 'Speed Improvement',
    icon: IconSpeedImprovement,
  },
  {
    id: 3,
    title: 'Accesories',
    icon: IconAccesories,
  },
]

const activePage = ref(2)

function next() {
  if (activePage.value < items.length)
    activePage.value++
}

function prev() {
  if (activePage.value > 1)
    activePage.value--
}
</script>

<template>
  <section id="our-speciality" class="bg-[#509FDD] px-5 pb-12 pt-9 text-center">
    <div class="bg-white px-8 py-11">
      <h1 class="text-primary mb-3 text-2xl font-bold uppercase">
        Our Speciality
      </h1>
      <p class="mb-8 text-sm font-light leading-6 text-[#303030]">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis euismod libero vel leo auctor, in venenatis nulla consequat. Sed commodo nunc sit amet congue aliquam.
      </p>
      <div class="overflow-x-hidden">
        <div class="mb-20 flex flex-nowrap mx-auto" :style="{ width: `${(50 * (items.length - 1)) + 300}px` }">
          <div
            v-for="item in items" :key="item.title"
            class="flex flex-col items-center justify-center gap-4 text-center"
            :style="{ width: activePage === item.id ? '300px' : '50px' }"
          >
            <component :is="item.icon" />
            <span>{{ item.title }}</span>
          </div>
        </div>
      </div>
      <p class="mb-20 text-center text-sm font-light leading-6 text-[#a7a7a7]">
        Lorem ipsum dolor sit amet, consectetur adipiscing elit. Duis euismod libero vel leo auctor, in venenatis nulla consequat. Sed commodo nunc sit amet congue aliquam.
      </p>
      <div class="flex items-center justify-between gap-2">
        <div
          class="i-carbon-arrow-left text-2xl"
          :class="activePage > 1 && activePage <= items.length ? 'cursor-pointer text-[#3D46A2]' : 'text-[#d2d2d2]'"
          @click="prev"
        />
        <div class="flex items-center gap-4">
          <div
            v-for="(dot, index) in items"
            :key="index"
            class="h-3 w-3 rounded-full bg-[#DAF3FC]"
            :class="{ 'border-2 border-[#3D46A2] bg-white': dot.id === activePage }"
          />
        </div>
        <div
          class="i-carbon-arrow-right text-2xl text-[#3D46A2]"
          :class="activePage < items.length ? 'cursor-pointer text-[#3D46A2]' : 'text-[#d2d2d2]'"
          @click="next"
        />
      </div>
    </div>
  </section>
</template>

<style scoped>

</style>
