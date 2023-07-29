<script setup lang="ts">
function scrollTo(id: string) {
  const element = document.getElementById(id)
  element?.scrollIntoView({ behavior: 'smooth' })
}
</script>

<template>
  <footer class="relative overflow-hidden bg-[#07477A] px-8 py-9">
    <div class="relative z-10">
      <LogoWhite class="mb-8" />
      <div class="mb-8 bg-white px-7 py-6">
        <div class="mb-10 flex items-center justify-between border border-[#C4C4C4] rounded px-4 py-3 text-sm">
          <span class="font-bold uppercase text-[#00537C]">TECHNOLOGY DEPARTMENT</span>
          <div class="i-carbon-chevron-down text-xl text-[#C4C4C4]" />
        </div>
        <div class="w-1/2 text-lg text-[#25A0D8]">
          Jl. Lembong No 8 Kel. Braga Kec. Sumur Bandung, Kota Bandung, Jawa Barat
        </div>
      </div>
      <div class="flex flex-col md:flex-row md:gap-6">
        <div class="cursor-pointer leading-[48px] text-white" @click="scrollTo('slider')">
          Who We Are
        </div>
        <div class="cursor-pointer leading-[48px] text-white" @click="scrollTo('our-values')">
          Our Values
        </div>
        <div class="cursor-pointer leading-[48px] text-white" @click="scrollTo('our-speciality')">
          The Perks
        </div>
      </div>
    </div>
    <FooterCover class="absolute left-0 z-0 h-auto w-full object-cover -bottom-30" />
  </footer>
</template>

<style scoped>

</style>
