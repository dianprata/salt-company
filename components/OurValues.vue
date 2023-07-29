<script setup lang="ts">

</script>

<template>
  <section id="our-values" class="pt-14">
    <h1 class="text-primary mb-6 px-6 text-center text-4xl font-medium">
      Our Core Values
    </h1>
    <p class="px-6 text-[#777]">
      Ridiculus laoreet libero pretium et, sit vel elementum convallis fames. Sit suspendisse etiam eget egestas. Aliquet odio et lectus etiam sit.
      <br> <br>
      In mauris rutrum ac ut volutpat, ornare nibh diam. Montes, vitae, nec amet enim.
    </p>
    <ul class="mb-7 mt-9 flex flex-col gap-6 pl-14 pr-4">
      <li>
        <h4 class="mb-3 text-2xl">
          Dedication
        </h4>
        <p class="text-[#777]">
          Nam libero tempore, cum soluta nobis est eligendi optio cumque nihil impedit quo minus id quod maxime placeat.
        </p>
      </li>
      <li>
        <h4 class="mb-3 text-2xl">
          Intellectual Honesty
        </h4>
        <p class="text-[#777]">
          Itaque earum rerum hic tenetur a sapiente delectus, ut aut reiciendis voluptatibus maiores alias conse.
        </p>
      </li>
      <li>
        <h4 class="mb-3 text-2xl">
          Curiosity
        </h4>
        <p class="text-[#777]">
          At vero eos et accusamus et iusto odio dignissimos ducimus qui blanditiis praesentium voluptatum deleniti atque.
        </p>
      </li>
    </ul>
    <img src="/core-values-illustration.svg" alt="" class="w-full">
  </section>
</template>

<style scoped>
#our-values ul li {
  position: relative;
}
#our-values ul li:before {
  content: '';
  position: absolute;
  left: -45px;
  top: 14px;
  display: block;
  width: 28px;
  height: 2px;
  background-color: #747474;
}
</style>
