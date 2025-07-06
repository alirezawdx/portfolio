<script setup lang="ts">
import SingleButton from '@/components/SingleButton.vue'
import Character from './../assets/imgs/character.webp'
import ProjectItem from '@/components/ProjectItem.vue'
import { ref } from 'vue'
import ServicesList from '@/layouts/ServicesList.vue'
import ContactForm from '@/layouts/ContactForm.vue'

const projects = ref([
  {
    img: 'https://static.roocket.ir/images/cover/2025/3/15/Pqu8W5Y0yhUn8AOvavG8a3jbNYH9vPKzac1VSywd.jpg',
    title: 'The First Project Item',
    tech: 'Vue / Tailwind',
  },
  {
    img: 'https://static.roocket.ir/images/cover/2023/12/1/bfXiSAuUHdHj6jI8sUsQx0j7MdTGRd3zF4O3Lyzc.jpg',
    title: 'The Second Project Item',
    tech: 'Nuxt / Tailwind',
  },
  {
    img: 'https://static.roocket.ir/images/cover/2023/12/1/DVR05FQ8KOVnKQSlBPBXxsWkx3dqqwhk7a3ibULR.jpg',
    title: 'The Third Project Item',
    tech: 'FastAPI / Tailwind',
  },
])
</script>

<template>
  <div
    class="relative min-h-96 my-24 inset-shadow-[0_0_50px_50px] inset-shadow-[#E0E8F6] flex flex-col gap-8 justify-center items-center text-center overflow-hidden"
  >
    <div class="bg-pattern min-h-96 py-40 absolute -z-10 duration-1000"></div>
    <img
      :src="Character"
      alt="Alireza Sadeghi"
      class="w-40 h-40 object-cover rounded-full shadow-2xl"
    />

    <h1 class="text-5xl font-extrabold font-[Montserrat] text-[#484E53] uppercase">
      Alireza Sadeghi
    </h1>
    <h2 class="text-2xl font-semibold font-[Montserrat] text-[#484E53] lowercase -mt-4">
      <span class="bg-gradient-to-r from-[#4FC3F7] to-[#484E53] bg-clip-text text-transparent">
        front-end magician
      </span>
      <span class="text-3xl">🧙‍♂️</span>
    </h2>
    <p class="text-[#484E53] max-w-3/4 md:max-w-1/2 -mt-4">
      As a passionate data scientist, with expertise in machine learning, AI, and data analytics, I
      thrive on the challenges of exploring complex data landscapes and uncovering meaningful
      patterns that drive innovation
    </p>

    <SingleButton href="/contact" shape="pill">Contact me</SingleButton>
  </div>

  <div name="#about" class="my-40 flex flex-col gap-8 justify-center items-center text-center">
    <h2 class="text-4xl font-extrabold font-[Montserrat] text-[#484E53] lowercase">
      <span class="text-[#4FC3F7] font-medium">/</span> about
    </h2>
    <h3 class="text-xl font-medium font-[Montserrat] text-[#484E53] lowercase -mt-5">
      <span class="bg-gradient-to-r from-[#4FC3F7] to-[#484E53] bg-clip-text text-transparent">
        Get to know me
      </span>
    </h3>
    <p class="text-[#484E53] max-w-3/4 md:max-w-1/2">
      Hi there! I'm [Your Name], a data scientist specializing in data analytics, predictive
      modeling, natural language processing, machine learning, and AI chatbots. With a passion for
      unraveling insights from complex datasets, I'm dedicated to helping businesses make informed
      decisions and stay ahead in today's data-driven world.
    </p>
    <p class="text-[#484E53] max-w-3/4 md:max-w-1/2">
      I bring a blend of technical expertise, hands-on experience, and a commitment to clear
      communication to every project. Whether it's uncovering hidden patterns, predicting future
      trends, or automating processes with AI, I'm here to help you harness the full potential of
      your data.
    </p>
    <p class="text-[#484E53] max-w-3/4 md:max-w-1/2">
      Let's work together to transform your data into actionable insights that drive real results.
      Get in touch, and let's start unlocking the power of your data today!
    </p>

    <SingleButton href="/contact" shape="pill">Downlaod Resume</SingleButton>
  </div>

  <div name="#projects" class="my-40 flex flex-col gap-8 justify-center items-center text-center">
    <h2 class="text-4xl font-extrabold font-[Montserrat] text-[#484E53] lowercase">
      <span class="text-[#4FC3F7] font-medium">/</span> projects
    </h2>
    <h3 class="text-xl font-medium font-[Montserrat] text-[#484E53] lowercase -mt-5">
      <span class="bg-gradient-to-r from-[#4FC3F7] to-[#484E53] bg-clip-text text-transparent">
        taste my vibe
      </span>
    </h3>

    <div class="flex flex-wrap">
      <ProjectItem
        v-for="project in projects"
        :key="project.title"
        class="w-full md:w-1/3 p-5"
        :img="project.img"
        :tech="project.tech"
        >{{ project.title }}</ProjectItem
      >
    </div>

    <SingleButton href="/contact" shape="pill">View All</SingleButton>
  </div>

  <div name="#services" class="my-40 flex flex-col gap-8 justify-center items-center text-center">
    <h2 class="text-4xl font-extrabold font-[Montserrat] text-[#484E53] lowercase">
      <span class="text-[#4FC3F7] font-medium">/</span> services
    </h2>
    <h3 class="text-xl font-medium font-[Montserrat] text-[#484E53] lowercase -mt-5">
      <span class="bg-gradient-to-r from-[#4FC3F7] to-[#484E53] bg-clip-text text-transparent">
        what i do
      </span>
    </h3>

    <ServicesList />
  </div>

  <div name="#contact" class="my-40 flex flex-col gap-8 justify-center items-center text-center">
    <h2 class="text-4xl font-extrabold font-[Montserrat] text-[#484E53] lowercase">
      <span class="text-[#4FC3F7] font-medium">/</span> contact
    </h2>
    <h3 class="text-xl font-medium font-[Montserrat] text-[#484E53] lowercase -mt-5">
      <span class="bg-gradient-to-r from-[#4FC3F7] to-[#484E53] bg-clip-text text-transparent">
        send me a message
      </span>
    </h3>

    <ContactForm />
  </div>
</template>

<style>
@keyframes move-bg {
  0% {
    transform: translateX(-4000px);
  }
  50% {
    transform: translateX(4000px);
  }
  100% {
    transform: translateX(-4000px);
  }
}

.bg-pattern {
  min-width: 10000px !important;
  animation-name: move-bg;
  animation-composition: ease-out;
  animation-duration: 500s;
  animation-iteration-count: infinite;
  background-position: center center;
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' version='1.1' xmlns:xlink='http://www.w3.org/1999/xlink' xmlns:svgjs='http://svgjs.dev/svgjs' width='10000' height='600' preserveAspectRatio='none' viewBox='0 0 10000 600'%3e%3cg mask='url(%26quot%3b%23SvgjsMask1091%26quot%3b)' fill='none'%3e%3crect width='10000' height='600' x='0' y='0' fill='rgba(224%2c 232%2c 246%2c 1)'%3e%3c/rect%3e%3cpath d='M -23.32347346935569%2c245 C 158.68%2c282.8 522.68%2c448.2 886.6765265306443%2c434 C 1250.68%2c419.8 1432.68%2c190.8 1796.6765265306444%2c174 C 2160.68%2c157.2 2342.68%2c337.2 2706.6765265306444%2c350 C 3070.68%2c362.8 3252.68%2c246.2 3616.6765265306444%2c238 C 3980.68%2c229.8 4162.68%2c313.8 4526.676526530644%2c309 C 4890.68%2c304.2 5072.68%2c181.6 5436.676526530644%2c214 C 5800.68%2c246.4 5982.68%2c454.2 6346.676526530644%2c471 C 6710.68%2c487.8 6892.68%2c310 7256.676526530644%2c298 C 7620.68%2c286 7802.68%2c426 8166.676526530644%2c411 C 8530.68%2c396 8712.68%2c209.4 9076.676526530644%2c223 C 9440.68%2c236.6 9622.68%2c467.6 9986.676526530644%2c479 C 10350.68%2c490.4 10894.01%2c294.2 10896.676526530644%2c280 C 10899.34%2c265.8 10179.34%2c382.4 10000%2c408' stroke='rgba(159%2c 159%2c 159%2c 0.37)' stroke-width='2'%3e%3c/path%3e%3cpath d='M -443.09861639625234%2c413 C -261.1%2c370.2 102.9%2c200.4 466.90138360374766%2c199 C 830.9%2c197.6 1012.9%2c386.4 1376.9013836037477%2c406 C 1740.9%2c425.6 1922.9%2c284.6 2286.9013836037475%2c297 C 2650.9%2c309.4 2832.9%2c478.2 3196.9013836037475%2c468 C 3560.9%2c457.8 3742.9%2c272.8 4106.9013836037475%2c246 C 4470.9%2c219.2 4652.9%2c349.2 5016.9013836037475%2c334 C 5380.9%2c318.8 5562.9%2c146.8 5926.9013836037475%2c170 C 6290.9%2c193.2 6472.9%2c445.8 6836.9013836037475%2c450 C 7200.9%2c454.2 7382.9%2c193.8 7746.9013836037475%2c191 C 8110.9%2c188.2 8292.9%2c418 8656.901383603748%2c436 C 9020.9%2c454 9202.9%2c306.2 9566.901383603748%2c281 C 9930.9%2c255.8 10390.28%2c322.4 10476.901383603748%2c310 C 10563.52%2c297.6 10095.38%2c237.2 10000%2c219' stroke='rgba(159%2c 159%2c 159%2c 0.37)' stroke-width='2'%3e%3c/path%3e%3cpath d='M -830.1754635053866%2c194 C -648.18%2c252 -284.18%2c476.6 79.82453649461338%2c484 C 443.82%2c491.4 625.82%2c257.8 989.8245364946134%2c231 C 1353.82%2c204.2 1535.82%2c365 1899.8245364946133%2c350 C 2263.82%2c335 2445.82%2c148.4 2809.8245364946133%2c156 C 3173.82%2c163.6 3355.82%2c367.4 3719.8245364946133%2c388 C 4083.82%2c408.6 4265.82%2c252.4 4629.824536494613%2c259 C 4993.82%2c265.6 5175.82%2c447 5539.824536494613%2c421 C 5903.82%2c395 6085.82%2c121.2 6449.824536494613%2c129 C 6813.82%2c136.8 6995.82%2c453.8 7359.824536494613%2c460 C 7723.82%2c466.2 7905.82%2c156.8 8269.824536494614%2c160 C 8633.82%2c163.2 8815.82%2c479.6 9179.824536494614%2c476 C 9543.82%2c472.4 9925.79%2c145.2 10089.824536494614%2c142 C 10253.86%2c138.8 10017.96%2c396.4 10000%2c460' stroke='rgba(159%2c 159%2c 159%2c 0.37)' stroke-width='2'%3e%3c/path%3e%3cpath d='M -369.9441006459008%2c155 C -187.94%2c217 176.06%2c469.6 540.0558993540992%2c465 C 904.06%2c460.4 1086.06%2c127.6 1450.0558993540992%2c132 C 1814.06%2c136.4 1996.06%2c457 2360.055899354099%2c487 C 2724.06%2c517 2906.06%2c302.6 3270.055899354099%2c282 C 3634.06%2c261.4 3816.06%2c386.2 4180.055899354099%2c384 C 4544.06%2c381.8 4726.06%2c254.6 5090.055899354099%2c271 C 5454.06%2c287.4 5636.06%2c466.4 6000.055899354099%2c466 C 6364.06%2c465.6 6546.06%2c268 6910.055899354099%2c269 C 7274.06%2c270 7456.06%2c482.8 7820.055899354099%2c471 C 8184.06%2c459.2 8366.06%2c240.4 8730.0558993541%2c210 C 9094.06%2c179.6 9276.06%2c334.4 9640.0558993541%2c319 C 10004.06%2c303.6 10478.07%2c124.8 10550.0558993541%2c133 C 10622.04%2c141.2 10110.01%2c314.6 10000%2c360' stroke='rgba(159%2c 159%2c 159%2c 0.37)' stroke-width='2'%3e%3c/path%3e%3c/g%3e%3cdefs%3e%3cmask id='SvgjsMask1091'%3e%3crect width='10000' height='600' fill='white'%3e%3c/rect%3e%3c/mask%3e%3c/defs%3e%3c/svg%3e");
}

select {
  -moz-appearance: none; /* Firefox */
  -webkit-appearance: none; /* Safari and Chrome */
  appearance: none;
}
</style>
