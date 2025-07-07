<script setup lang="ts">
const { emoji } = defineProps<{
  emoji: string
}>()
</script>

<template>
  <svg class="w-10 h-10" xmlns="http://www.w3.org/2000/svg">
    <image :href="emoji" class="w-full h-full" />
  </svg>
</template>
