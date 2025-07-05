<script setup lang="ts">
import MenuItem from './MenuItem.vue'

const props = defineProps({
  links: Array,
})
</script>

<template>
  <ul class="flex items-center">
    <MenuItem v-for="link in props.links" :href="link.href">
      {{ link.text }}
    </MenuItem>
  </ul>
</template>
