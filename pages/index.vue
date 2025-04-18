<script setup lang="ts">
import { motion } from "motion-v";
useHead({
  title: "Evan SENDE",
});
</script>

<template>
  <div class="bg-[#FCFCFC]">
    <motion.div
      :initial="{ opacity: 0, scale: 0.8 }"
      :while-in-view="{ opacity: 1, scale: 1 }"
      :in-view-options="{ once: true }"
      :transition="{ duration: 0.5 }"
    >
      <Hero></Hero
    ></motion.div>
    <motion.div
      :initial="{ opacity: 0, scale: 0.8 }"
      :while-in-view="{ opacity: 1, scale: 1 }"
      :in-view-options="{ once: true }"
      :transition="{ duration: 0.5 }"
    >
      <VideoSection></VideoSection
    ></motion.div>
    <motion.div
      :initial="{ opacity: 0, scale: 0.8 }"
      :while-in-view="{ opacity: 1, scale: 1 }"
      :in-view-options="{ once: true }"
      :transition="{ duration: 0.5 }"
    >
      <Work></Work
    ></motion.div>
    <motion.div
      :initial="{ opacity: 0, scale: 0.8 }"
      :while-in-view="{ opacity: 1, scale: 1 }"
      :in-view-options="{ once: true }"
      :transition="{ duration: 0.5 }"
    >
      <Call></Call><Footer></Footer>
    </motion.div>
  </div>
</template>

<style>
.box {
  width: 100px;
  height: 100px;
  background-color: #0cdcf7;
  border-radius: 5px;
}
</style>
