<script setup lang="ts">
interface Items {
  title: string
  subTitle: string
  description: string
}
defineProps<{
  items: Items[]
  currentPage: number
}>()

const emit = defineEmits(['click:next', 'click:prev'])

function next() {
  emit('click:next')
}
function prev() {
  emit('click:prev')
}
</script>

<template>
  <div class="bg-white px-10 py-12 -mt-6">
    <template v-for="(item, index) in items" :key="index">
      <div v-if="index + 1 === currentPage" class="mb-20">
        <h1 class="text-primary mb-3 text-4xl font-medium">
          {{ item.title }}
        </h1>
        <h5 class="text-lg leading-9">
          {{ item.subTitle }}
        </h5>
        <p class="leading-6 text-[#777]">
          {{ item.description }}
        </p>
      </div>
    </template>
    <div class="flex items-center justify-between gap-2">
      <div class="flex items-end gap-1.5">
        <span class="text-2xl text-[#303030]">0{{ currentPage }}</span>
        <span class="text-2xl text-[#C0C0C0]">/</span>
        <span class="text-[#C0C0C0]">0{{ items.length }}</span>
      </div>
      <div class="flex items-center">
        <div
          class="cursor-pointer p-3"
          :class="currentPage > 1 && currentPage <= items.length ? 'bg-primary text-white' : 'bg-[#f1f1f1] text-[#B6B6B6]'"
          @click="prev"
        >
          <span class="i-carbon-arrow-left block" />
        </div>
        <div
          class="cursor-pointer p-3"
          :class="currentPage < items.length ? 'bg-primary text-white' : 'bg-[#f1f1f1] text-[#B6B6B6]'"
          @click="next"
        >
          <span class="i-carbon-arrow-right block" />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>

</style>
