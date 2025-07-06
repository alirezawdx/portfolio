<script setup lang="ts">
import SiteLogo from '@/components/SiteLogo.vue'
import MenuList from '../components/MenuList.vue'
import SingleButton from '@/components/SingleButton.vue'
import DarkModeButton from '@/components/DarkModeButton.vue'

import { ref, onMounted } from 'vue'

const menuOpen = ref(false)
const shadowForNavbar = ref(false)

const links = [
  { text: 'Home', href: '/' },
  { text: 'About', href: '/about' },
  { text: 'Projects', href: '/projects' },
  { text: 'Services', href: '/services' },
  { text: 'Resume', href: '/resume' },
]

onMounted(() => {
  window.addEventListener('scroll', () => {
    shadowForNavbar.value = window.scrollY >= 50
  })
})
</script>

<template>
  <div
    class="w-full p-5 -mt-20 fixed z-50 left-[50%] translate-x-[-50%] duration-150 bg-[#E0E8F6]"
    :class="shadowForNavbar ? 'shadow-md' : ''"
  >
    <header class="container mx-auto flex justify-between items-center">
      <SiteLogo class="w-24" />

      <nav>
        <MenuList :links="links" class="gap-12 hidden md:flex"></MenuList>
      </nav>

      <SingleButton class="hidden md:inline" href="/contact">Contact</SingleButton>

      <DarkModeButton class="hidden md:inline-block" />

      <transition mode="out-in">
        <svg
          v-if="!menuOpen"
          @click="menuOpen = !menuOpen"
          class="md:hidden w-6 h-6 text-gray-800 dark:text-white rotate-180"
          aria-hidden="true"
          xmlns="http://www.w3.org/2000/svg"
          width="24"
          height="24"
          fill="none"
          viewBox="0 0 24 24"
        >
          <path
            stroke="currentColor"
            stroke-linecap="round"
            stroke-width="2"
            d="M5 7h14M5 12h14M5 17h10"
          />
        </svg>
      </transition>

      <transition>
        <div
          v-show="menuOpen"
          class="bg-[#E0E8F6] w-full h-full fixed top-0 left-0 flex justify-start items-start flex-col gap-6 p-12 z-50"
        >
          <div class="flex gap-2 justify-between items-center w-full mb-12">
            <SiteLogo class="h-8" />

            <div>
              <DarkModeButton class="" />
              <button
                class="p-3 cursor-pointer text-[#484E53] hover:bg-[#e1e1e1] duration-150 rounded-lg"
                @click="menuOpen = false"
              >
                <svg
                  class="w-6 h-6 text-gray-800 dark:text-white"
                  aria-hidden="true"
                  xmlns="http://www.w3.org/2000/svg"
                  width="24"
                  height="24"
                  fill="none"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke="currentColor"
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M6 18 17.94 6M18 18 6.06 6"
                  />
                </svg>
              </button>
            </div>
          </div>

          <nav>
            <MenuList :links="links" class="gap-8"></MenuList>
          </nav>

          <SingleButton class="mt-8 w-full text-center">Contact</SingleButton>
        </div></transition
      >
    </header>
  </div>
</template>

<style>
.v-enter-active,
.v-leave-active {
  transition: opacity 0.2s ease;
}

.v-enter-from,
.v-leave-to {
  opacity: 0;
}
</style>
