<script setup lang="ts">
import SiteLogo from '@/components/SiteLogo.vue'
import MenuList from '../components/MenuList.vue'
import SingleButton from '@/components/SingleButton.vue'
import DarkModeButton from '@/components/DarkModeButton.vue'

const links = [
  { text: 'Home', href: '/' },
  { text: 'About', href: '/about' },
  { text: 'Projects', href: '/projects' },
  { text: 'Services', href: '/services' },
  { text: 'Resume', href: '/resume' },
]
</script>

<template>
  <header class="flex justify-between items-center">
    <SiteLogo class="w-24" />

    <nav>
      <MenuList :links="links" class="gap-12"></MenuList>
    </nav>

    <SingleButton href="/contact">Contact</SingleButton>

    <DarkModeButton />
  </header>
</template>
