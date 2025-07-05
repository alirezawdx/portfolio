<script setup lang="ts">
const props = defineProps({
  href: String,
})
</script>

<template>
  <li>
    <a :href="props.href" class="text-[#050505] hover:text-[#4FC3F7] duration-150 p-0 m-0">
      <slot></slot>
    </a>
  </li>
</template>
