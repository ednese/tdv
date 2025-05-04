<script setup lang="ts">
import { motion } from "motion-v";
</script>

<template>
  <nav
    class="top-0 p-8 z-10 w-full absolute bg-gradient-to-b from-gray-800 to-transparent"
  >
    <motion.div
      class="hidden lg:flex justify-between items-center text-slate-400 text-lg"
    >
      <NuxtLink to="/">
        <motion.p
          :initial="{ opacity: 0, y: -10 }"
          :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.7, delay: 1 }"
          >Evan Sende</motion.p
        >
      </NuxtLink>
      <div>
        <motion.img
          :initial="{ opacity: 0, y: -10 }"
          :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.7, delay: 1.5 }"
          src="/img/ednese_logo_white.svg"
          class="absolute w-4 self-center left-1/2 transform -translate-x-1/2"
        />
        <motion.div
          :initial="{ opacity: 0, y: -10 }"
          :animate="{ opacity: 1, y: 0 }"
          :transition="{ duration: 0.7, delay: 2 }"
        >
          <NuxtLink
            to="https://cal.com/evansende/qualification-freelance?overlayCalendar=true&duration=15"
            target="_blank"
            class="uppercase px-5 py-3 bg-slate-200 text-sm rounded-full flex items-center h-fit text-black"
          >
            prendre un rendez-vous
          </NuxtLink></motion.div
        >
      </div>
    </motion.div>
  </nav>
</template>
