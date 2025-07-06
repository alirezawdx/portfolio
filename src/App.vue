<script setup lang="ts">
import FooterLayout from './layouts/FooterLayout.vue'
import NavbarMenu from './layouts/NavbarMenu.vue'
import HomeView from './views/HomeView.vue'
</script>

<template>
  <div class="container mx-auto pt-20">
    <NavbarMenu />

    <main>
      <HomeView />
    </main>
  </div>
  <FooterLayout />
</template>
