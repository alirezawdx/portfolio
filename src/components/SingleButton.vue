<script setup lang="ts">
const props = defineProps({
  href: String,
  shape: String,
})
</script>

<template>
  <a
    :href="href"
    :class="shape == 'pill' ? 'rounded-full py-3 w-52' : 'rounded-lg py-2 px-5'"
    class="border-2 border-[#484E53] font-light hover:bg-[#4FC3F7] hover:border-[#4FC3F7] duration-150 hover:text-white"
  >
    <slot></slot>
  </a>
</template>
