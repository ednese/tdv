<script setup lang="ts">
import { SpeedInsights } from "@vercel/speed-insights/vue";
import { Analytics } from "@vercel/analytics/nuxt";
</script>

<template>
  <div>
    <Analytics />
    <SpeedInsights />
    <NuxtPage />
  </div>
</template>
