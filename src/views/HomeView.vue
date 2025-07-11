<script setup lang="ts">
import { ref } from 'vue'
import SingleButton from '@/components/SingleButton.vue'
import Character from './../assets/imgs/me-2.jpeg'
import Emoji from './../assets/imgs/magician.png'
import ProjectItem from '@/components/ProjectItem.vue'
import ServicesList from '@/layouts/ServicesList.vue'
import ContactForm from '@/layouts/ContactForm.vue'
import SVGEmoji from '@/components/SVGEmoji.vue'

const projects = ref([
  {
    img: 'https://static.roocket.ir/images/cover/2025/3/15/Pqu8W5Y0yhUn8AOvavG8a3jbNYH9vPKzac1VSywd.jpg',
    title: 'The First Project Item',
    tech: 'Vue / Tailwind',
  },
])
</script>

<template>
  <div
    class="relative min-h-96 my-24 inset-shadow-[0_0_50px_50px] duration-150 inset-shadow-[#E0E8F6] dark:inset-shadow-[#1E1E1E] flex flex-col gap-8 justify-center items-center text-center overflow-hidden"
  >
    <div class="bg-pattern min-h-96 py-40 absolute -z-10 duration-1000"></div>
    <img
      :src="Character"
      alt="Alireza Sadeghi"
      class="w-40 h-40 object-cover rounded-full shadow-2xl"
    />

    <h1 class="text-5xl font-extrabold font-[Montserrat] text-[#484E53] dark:text-white uppercase">
      Alireza Sadeghi
    </h1>
    <h2 class="text-2xl font-semibold font-[Montserrat] text-[#484E53] lowercase -mt-4">
      <span
        class="flex justify-center items-center gap-1 bg-gradient-to-r from-[#4FC3F7] to-[#484E53] dark:to-[#C1C1C1] bg-clip-text text-transparent"
      >
        front-end magician
        <SVGEmoji :emoji="Emoji" />
      </span>
    </h2>
    <p class="text-[#484E53] px-5 w-full md:max-w-1/2 -mt-4 dark:text-[#C1C1C1]">
      Hi, I’m a <strong>frontend</strong> developer who loves crafting smooth, responsive user
      experiences — but I’m also no stranger to the <strong>backend</strong>. From building clean
      UIs with <a href="https://vuejs.org" class="text-green-400">Vue.js</a> to setting up APIs and
      managing databases, I enjoy working across the stack to bring ideas to life. Whether it’s a
      personal project or a team collaboration, I’m always up for solving problems and turning
      concepts into real, usable products.
    </p>

    <SingleButton href="tel:+989050989004" shape="pill" class="dark:text-white"
      >Send me a text</SingleButton
    >
  </div>

  <div name="#about" class="my-40 flex flex-col gap-8 justify-center items-center text-center">
    <h2 class="text-4xl font-extrabold font-[Montserrat] text-[#484E53] lowercase dark:text-white">
      <span class="text-[#4FC3F7] font-medium">/</span> about
    </h2>
    <h3 class="text-xl font-medium font-[Montserrat] text-[#484E53] lowercase -mt-5">
      <span
        class="bg-gradient-to-r dark:to-[#C1C1C1] from-[#4FC3F7] to-[#484E53] bg-clip-text text-transparent"
      >
        Get to know me
      </span>
    </h3>
    <p class="text-[#484E53] w-full px-5 md:max-w-1/2 dark:text-[#C1C1C1]">
      I'm a 24-year-old developer with a passion for building web applications that are fast, clean,
      and functional. I mainly work with Vue.js on the frontend and FastAPI or Django on the
      backend, giving me the flexibility to handle both sides of a project when needed.
    </p>
    <p class="text-[#484E53] w-full px-5 md:max-w-1/2 dark:text-[#C1C1C1]">
      I'm comfortable using Git for version control, and I have a basic grasp of server management,
      especially on Linux, which is my favorite OS to work with. I enjoy learning new tools and
      frameworks, and I'm always looking for ways to improve my skills — whether it's diving deeper
      into backend logic or refining UI/UX details.
    </p>
    <p class="text-[#484E53] w-full px-5 md:max-w-1/2 dark:text-[#C1C1C1]">
      English isn’t my first language, but I’m quite fluent and confident when working with
      international teams, reading docs, or writing clean, readable code comments and documentation.
    </p>

    <SingleButton href="https://flowcv.com/resume/m2hbmojherc6" shape="pill" class="dark:text-white"
      >Downlaod My CV</SingleButton
    >
  </div>

  <div name="#projects" class="my-40 flex flex-col gap-8 justify-center items-center text-center">
    <h2 class="text-4xl font-extrabold font-[Montserrat] text-[#484E53] lowercase dark:text-white">
      <span class="text-[#4FC3F7] font-medium">/</span> projects
    </h2>
    <h3 class="text-xl font-medium font-[Montserrat] text-[#484E53] lowercase -mt-5">
      <span
        class="bg-gradient-to-r dark:to-[#C1C1C1] from-[#4FC3F7] to-[#484E53] bg-clip-text text-transparent"
      >
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
      >
        {{ project.title }}
      </ProjectItem>
    </div>

    <SingleButton href="/contact" shape="pill" class="dark:text-white"
      >Go to <span class="underline">github.com</span></SingleButton
    >
  </div>

  <div name="#services" class="my-40 flex flex-col gap-8 justify-center items-center text-center">
    <h2 class="text-4xl font-extrabold font-[Montserrat] text-[#484E53] lowercase dark:text-white">
      <span class="text-[#4FC3F7] font-medium">/</span> services
    </h2>
    <h3 class="text-xl font-medium font-[Montserrat] text-[#484E53] lowercase -mt-5">
      <span
        class="bg-gradient-to-r dark:to-[#C1C1C1] from-[#4FC3F7] to-[#484E53] bg-clip-text text-transparent"
      >
        what i do
      </span>
    </h3>

    <ServicesList />
  </div>

  <div name="#contact" class="my-40 flex flex-col gap-8 justify-center items-center text-center">
    <h2 class="text-4xl font-extrabold font-[Montserrat] text-[#484E53] lowercase dark:text-white">
      <span class="text-[#4FC3F7] font-medium">/</span> contact
    </h2>
    <h3 class="text-xl font-medium font-[Montserrat] text-[#484E53] lowercase -mt-5">
      <span
        class="bg-gradient-to-r dark:to-[#C1C1C1] from-[#4FC3F7] to-[#484E53] bg-clip-text text-transparent"
      >
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
  background-image: url("data:image/svg+xml,%3csvg xmlns='http://www.w3.org/2000/svg' version='1.1' xmlns:xlink='http://www.w3.org/1999/xlink' xmlns:svgjs='http://svgjs.dev/svgjs' width='10000' height='600' preserveAspectRatio='none' viewBox='0 0 10000 600'%3e%3cg mask='url(%26quot%3b%23SvgjsMask1002%26quot%3b)' fill='none'%3e%3cpath d='M -573.2675044083022%2c175 C -391.27%2c226.6 -27.27%2c435.6 336.7324955916978%2c433 C 700.73%2c430.4 882.73%2c183 1246.732495591698%2c162 C 1610.73%2c141 1792.73%2c303.2 2156.732495591698%2c328 C 2520.73%2c352.8 2702.73%2c265.6 3066.732495591698%2c286 C 3430.73%2c306.4 3612.73%2c445.2 3976.732495591698%2c430 C 4340.73%2c414.8 4522.73%2c198.6 4886.732495591697%2c210 C 5250.73%2c221.4 5432.73%2c495 5796.732495591697%2c487 C 6160.73%2c479 6342.73%2c204 6706.732495591697%2c170 C 7070.73%2c136 7252.73%2c317.2 7616.732495591697%2c317 C 7980.73%2c316.8 8162.73%2c169 8526.732495591697%2c169 C 8890.73%2c169 9072.73%2c315.6 9436.732495591697%2c317 C 9800.73%2c318.4 10234.08%2c165.4 10346.732495591697%2c176 C 10459.39%2c186.6 10069.35%2c331.2 10000%2c370' stroke='rgba(199%2c 199%2c 199%2c 0.28)' stroke-width='2'%3e%3c/path%3e%3cpath d='M -1597.3396065207135%2c154 C -1415.34%2c208.2 -1051.34%2c399.2 -687.3396065207135%2c425 C -323.34%2c450.8 -141.34%2c303 222.66039347928654%2c283 C 586.66%2c263 768.66%2c325.2 1132.6603934792865%2c325 C 1496.66%2c324.8 1678.66%2c261.2 2042.6603934792865%2c282 C 2406.66%2c302.8 2588.66%2c440.8 2952.6603934792865%2c429 C 3316.66%2c417.2 3498.66%2c246.6 3862.6603934792865%2c223 C 4226.66%2c199.4 4408.66%2c310.4 4772.6603934792865%2c311 C 5136.66%2c311.6 5318.66%2c206 5682.6603934792865%2c226 C 6046.66%2c246 6228.66%2c400.8 6592.6603934792865%2c411 C 6956.66%2c421.2 7138.66%2c287 7502.6603934792865%2c277 C 7866.66%2c267 8048.66%2c387.6 8412.660393479287%2c361 C 8776.66%2c334.4 9005.19%2c148.4 9322.660393479287%2c144 C 9640.13%2c139.6 9864.53%2c300 10000%2c339' stroke='rgba(199%2c 199%2c 199%2c 0.28)' stroke-width='2'%3e%3c/path%3e%3cpath d='M -1281.9892665352381%2c460 C -1099.99%2c393.4 -735.99%2c140.2 -371.989266535238%2c127 C -7.99%2c113.8 174.01%2c386.8 538.010733464762%2c394 C 902.01%2c401.2 1084.01%2c165 1448.0107334647619%2c163 C 1812.01%2c161 1994.01%2c367.2 2358.010733464762%2c384 C 2722.01%2c400.8 2904.01%2c257.6 3268.010733464762%2c247 C 3632.01%2c236.4 3814.01%2c322.8 4178.010733464762%2c331 C 4542.01%2c339.2 4724.01%2c271.2 5088.010733464762%2c288 C 5452.01%2c304.8 5634.01%2c449.2 5998.010733464762%2c415 C 6362.01%2c380.8 6544.01%2c107.6 6908.010733464762%2c117 C 7272.01%2c126.4 7454.01%2c435 7818.010733464762%2c462 C 8182.01%2c489 8364.01%2c282.4 8728.010733464762%2c252 C 9092.01%2c221.6 9383.61%2c320.6 9638.010733464762%2c310 C 9892.41%2c299.4 9927.6%2c221.2 10000%2c199' stroke='rgba(199%2c 199%2c 199%2c 0.28)' stroke-width='2'%3e%3c/path%3e%3cpath d='M -259.3873041177908%2c125 C -77.39%2c179 286.61%2c375.8 650.6126958822092%2c395 C 1014.61%2c414.2 1196.61%2c231 1560.6126958822092%2c221 C 1924.61%2c211 2106.61%2c357.8 2470.612695882209%2c345 C 2834.61%2c332.2 3016.61%2c138.4 3380.612695882209%2c157 C 3744.61%2c175.6 3926.61%2c424.8 4290.61269588221%2c438 C 4654.61%2c451.2 4836.61%2c221.8 5200.61269588221%2c223 C 5564.61%2c224.2 5746.61%2c440.4 6110.61269588221%2c444 C 6474.61%2c447.6 6656.61%2c265 7020.61269588221%2c241 C 7384.61%2c217 7566.61%2c324.4 7930.61269588221%2c324 C 8294.61%2c323.6 8476.61%2c231.6 8840.61269588221%2c239 C 9204.61%2c246.4 9386.61%2c382.2 9750.61269588221%2c361 C 10114.61%2c339.8 10610.74%2c140.4 10660.61269588221%2c133 C 10710.49%2c125.6 10132.12%2c285.8 10000%2c324' stroke='rgba(199%2c 199%2c 199%2c 0.28)' stroke-width='2'%3e%3c/path%3e%3c/g%3e%3cdefs%3e%3cmask id='SvgjsMask1002'%3e%3crect width='10000' height='600' fill='white'%3e%3c/rect%3e%3c/mask%3e%3c/defs%3e%3c/svg%3e");
}

select {
  -moz-appearance: none; /* Firefox */
  -webkit-appearance: none; /* Safari and Chrome */
  appearance: none;
}
</style>
