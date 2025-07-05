<script setup lang="ts">
const props = defineProps({
  href: String,
})
</script>

<template>
  <a
    :href="href"
    class="border-2 border-[#484E53] rounded-lg py-2 px-5 font-light hover:bg-[#4FC3F7] hover:border-[#4FC3F7] duration-150 hover:text-white"
  >
    <slot></slot>
  </a>
</template>
