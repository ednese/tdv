<script setup lang="ts">
import { Analytics } from "@vercel/analytics/nuxt";

useHead({
  title: "Evan SENDE",
});
</script>

<template>
  <Analytics />
  <div class="pt-0 sm:pt-16 lg:pt-32">
    <Nav></Nav>
    <Hero></Hero>
    <VideoSection></VideoSection>
    <!-- Background -->
    <div
      class="absolute fixed inset-0 -z-10 h-full w-full items-center px-5 py-24 [background:radial-gradient(125%_125%_at_50%_10%,#000_40%,#63e_100%)]"
    ></div>
    <!-- Background -->
    <!-- <WorkPrenium></WorkPrenium> -->
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
