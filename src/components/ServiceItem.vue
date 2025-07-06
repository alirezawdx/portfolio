<script setup lang="ts">
const { title } = defineProps({
  title: String,
  img: String,
})
</script>

<template>
  <div class="p-3 flex-grow">
    <div
      class="h-full flex-wrap gap-5 md:flex-nowrap rounded-xl border border-white bg-white p-8 bg-gradient-to-br from-[#fbffff] to-[#e5edfa] flex justify-between items-start"
    >
      <div class="flex justify-start items-start flex-col gap-5">
        <div class="w-12 h-12 rounded-lg bg-[#bce7fa] flex justify-center items-center">
          <slot name="icon"></slot>
        </div>
        <h3 class="mt-2 text-xl text-[#484E53] font-semibold">{{ title }}</h3>
        <p>
          <slot name="description"></slot>
        </p>
      </div>
      <div v-if="img" class="h-full w-full">
        <img :src="img" class="h-full w-full object-cover rounded-lg" :alt="title" />
      </div>
    </div>
  </div>
</template>
