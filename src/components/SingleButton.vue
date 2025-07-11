<script setup lang="ts">
const { href, shape } = defineProps({
  href: String,
  shape: String,
  t: String,
})
</script>

<template>
  <a
    v-if="t != 'formSubmit'"
    :href="href"
    :class="shape == 'pill' ? 'rounded-full py-3 w-52' : 'rounded-lg py-2 px-5'"
    class="border-2 border-[#484E53] dark:border-[#4FC3F7] font-light hover:bg-[#4FC3F7] hover:border-[#4FC3F7] duration-150 hover:text-white"
  >
    <slot></slot>
  </a>
  <button
    v-else
    type="submit"
    :class="shape == 'pill' ? 'rounded-full py-3 w-52' : 'rounded-lg py-2 px-5'"
    class="border-2 border-[#484E53] dark:border-[#4FC3F7] font-light hover:bg-[#4FC3F7] hover:border-[#4FC3F7] duration-150 hover:text-white"
  >
    <slot></slot>
  </button>
</template>
