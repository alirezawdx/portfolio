<script setup lang="ts">
import NavbarMenu from './layouts/NavbarMenu.vue'
import HomeView from './views/HomeView.vue'
</script>

<template>
  <div class="container mx-auto py-12">
    <NavbarMenu />

    <main>
      <HomeView />
    </main>
  </div>
</template>
