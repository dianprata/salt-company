<script setup lang="ts">
import OurSpeciality from '~/components/OurSpeciality.vue'
import OurValues from '~/components/OurValues.vue'

const sliderItems = [
  {
    title: 'Who we are',
    subTitle: 'Technology Company',
    description: 'Sed ut perspiciatis unde omnis iste natus sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi architecto beatae vitae dicta sunt explicabo.',
  },
  {
    title: 'What we do',
    subTitle: 'Professional Brand Management',
    description: 'Neque porro quisquam est, qui dolorem ipsum quia dolor sit amet, consectetur, adipisci velit, sed quia non numquam eius modi tempora incidunt ut labore et dolore magnam aliquam quaerat voluptatem.',
  },
  {
    title: 'How we do',
    subTitle: 'Strategize, Design, Collaborate',
    description: 'Ut enim ad minima veniam, quis nostrum exercitationem ullam corporis suscipit laboriosam, nisi ut aliquid ex ea commodi consequatur? Quis autem vel eum iure reprehenderit qui in ea voluptate velit esse sequam nihil molestiae consequatur.',
  },
]
const currentPageSlider = ref(1)
</script>

<template>
  <div>
    <Hero />
    <Slider
      id="slider"
      class="relative z-50"
      :items="sliderItems" :current-page="currentPageSlider"
      @click:next="currentPageSlider += 1"
      @click:prev="currentPageSlider -= 1"
    />
    <OurValues />
    <OurSpeciality />
  </div>
</template>

<style scoped lang="scss">

</style>
