<script setup lang="ts">
import { ref } from 'vue'

const services = ref([
  {
    id: 0,
    title: 'Front-end Development',
    boxSize: '3',
    icon: 'M12 15v5m-3 0h6M4 11h16M5 15h14a1 1 0 0 0 1-1V5a1 1 0 0 0-1-1H5a1 1 0 0 0-1 1v9a1 1 0 0 0 1 1Z',
    description: 'Vue.js-based UI development with focus on performance and usability.',
  },
  {
    id: 1,
    title: 'Back-end Development',
    boxSize: '3',
    icon: 'm8 8-4 4 4 4m8 0 4-4-4-4m-2-3-4 14',
    description:
      'APIs and backend logic built with FastAPI or Django — clean, efficient, and ready to scale.',
  },
  {
    id: 2,
    title: 'Database Management',
    boxSize: '3',
    icon: 'M19 6c0 1.657-3.134 3-7 3S5 7.657 5 6m14 0c0-1.657-3.134-3-7-3S5 4.343 5 6m14 0v6M5 6v6m0 0c0 1.657 3.134 3 7 3s7-1.343 7-3M5 12v6c0 1.657 3.134 3 7 3s7-1.343 7-3v-6',
    description:
      'Experienced with designing, querying, and integrating SQL databases into web applications.',
  },
  {
    id: 3,
    title: 'Telegram Bot Development',
    boxSize: '1',
    icon: 'M9 17h6l3 3v-3h2V9h-2M4 4h11v8H9l-3 3v-3H4V4Z',
    description:
      'I build smart and efficient Telegram bots using Python, perfect for automation, notifications, and user interaction.',
  },
  {
    id: 4,
    title: 'AI-Powered Solutions',
    boxSize: '3',
    icon: 'M12 15v5m-3 0h6M4 11h16M5 15h14a1 1 0 0 0 1-1V5a1 1 0 0 0-1-1H5a1 1 0 0 0-1 1v9a1 1 0 0 0 1 1Z',
    description: 'Enhancing applications with smart, AI-powered features when needed.',
  },
])
</script>

<template>
  <div class="flex flex-wrap w-full text-left">
    <ServiceItem
      v-for="service in services"
      :key="service.id"
      :title="service.title"
      :class="service.boxSize == '3' ? 'basis-1/3' : 'basis-2/3'"
    >
      <template v-slot:icon>
        <svg
          class="w-6 h-6 text-gray-800"
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
            :d="service.icon"
          />
        </svg>
      </template>
      <template v-slot:description>
        {{ service.description }}
      </template>
    </ServiceItem>
  </div>
</template>
