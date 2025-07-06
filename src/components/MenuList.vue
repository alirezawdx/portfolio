<script setup lang="ts">
import MenuItem from './MenuItem.vue'

const props = defineProps<{
  links: Array<{
    href: string
    text: string
  }>
}>()
</script>

<template>
  <ul
    class="flex items-start md:items-center justify-start md:justify-between flex-col md:flex-row"
  >
    <MenuItem v-for="link in props.links" :key="link.href" :href="link.href">
      {{ link.text }}
    </MenuItem>
  </ul>
</template>
