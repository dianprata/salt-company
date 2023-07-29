<script setup lang="ts">
import ScrollToBottom from '~/components/icon/ScrollToBottom.vue'
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

function scrollToSlider() {
  const slider = document.getElementById('slider')
  slider?.scrollIntoView({ behavior: 'smooth' })
}
</script>

<template>
  <div>
    <Hero />
    <ScrollToBottom class="relative z-100 mx-auto cursor-pointer" @click="scrollToSlider" />
    <Slider
      id="slider"
      :items="sliderItems" :current-page="currentPageSlider"
      @click:next="currentPageSlider += 1"
      @click:prev="currentPageSlider -= 1"
    />
    <OurValues />
    <OurSpeciality />
  </div>
</template>
