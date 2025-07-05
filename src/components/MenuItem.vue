<script setup lang="ts">
const props = defineProps({
  href: String,
})
</script>

<template>
  <li class="lowercase">
    <a
      :href="props.href"
      class="text-[#050505] hover:text-[#4FC3F7] font-medium duration-150 p-0 m-0 hidden md:inline-block"
    >
      <span class="text-[#4FC3F7] me-1">/</span> <slot></slot>
    </a>
    <h3 class="text-2xl font-semibold md:hidden">
      <span class="text-[#4FC3F7] me-3 font-light">/</span>
      <a :href="props.href"><slot></slot></a>
    </h3>
  </li>
</template>
