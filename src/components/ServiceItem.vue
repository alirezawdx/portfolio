<script setup lang="ts">
const { title } = defineProps({
  title: String,
  img: String,
})
</script>

<template>
  <div class="p-3 flex-grow">
    <div
      class="h-full flex-wrap gap-5 md:flex-nowrap rounded-xl border border-white dark:border-[#343434] bg-white p-8 bg-gradient-to-br from-[#fbffff] to-[#e5edfa] dark:from-[#282828] dark:to-[#1f1f1f] flex justify-between items-start"
    >
      <div class="flex justify-start items-start flex-col gap-5">
        <div
          class="w-12 h-12 rounded-lg bg-[#bce7fa] dark:bg-white flex justify-center items-center"
        >
          <slot name="icon"></slot>
        </div>
        <h3 class="mt-2 text-xl text-[#484E53] dark:text-[#E1E1E1] font-semibold">{{ title }}</h3>
        <p class="dark:text-[#c7c7c7]">
          <slot name="description"></slot>
        </p>
      </div>
      <div v-if="img" class="h-full w-full">
        <img :src="img" class="h-full w-full object-cover rounded-lg" :alt="title" />
      </div>
    </div>
  </div>
</template>
