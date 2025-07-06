<script setup lang="ts">
import SingleButton from './SingleButton.vue'

const { img, tech } = defineProps({ img: String, tech: String })
</script>

<template>
  <div
    class="text-left border border-transparent hover:border-[#484E53] dark:hover:border-[#C1C1C1] duration-200 rounded-2xl hover:shadow-2xl hover:-translate-y-2"
  >
    <img :src="img" alt="" class="rounded-xl shadow-xl" />

    <div class="flex justify-between items-center mt-5">
      <div>
        <h4 class="text-xl font-semibold dark:text-white">
          <slot></slot>
        </h4>
        <p class="text-[#484E53] dark:text-[#C1C1C1]">{{ tech }}</p>
      </div>
      <SingleButton href="/meow" class="dark:text-white">view</SingleButton>
    </div>
  </div>
</template>
