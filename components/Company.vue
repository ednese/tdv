<script setup lang="ts">
import { NuxtLink } from "#components";
const logos = ["matchem", "ca", "backmarket", "fifteen", "askup"];

defineProps<{
  logo: string;
  name: string;
  text: string;
  skills: string[];
  testimonial: {
    text: string;
    author: string;
  };
  url: string;
}>();
</script>

<template>
  <div class="flex items-start flex-col gap-4 max-w-[465px]">
    <div class="flex items-center gap-2 text-xl lg:text-3xl font-semibold">
      <img :src="logo" :alt="logo" height="40" />
      <h3>{{ name }}</h3>
    </div>
    <p class="text-start">{{ text }}</p>
    <div class="flex flex-wrap gap-2">
      <div
        v-for="skill in skills"
        class="border-solid border-2 border-slate-200 text-sm w-fit px-4 py-2 rounded-full"
      >
        {{ skill }}
      </div>
    </div>
    <div class="text-start bg-white p-4 rounded-xl flex flex-col gap-4">
      <div class="text-xs text-slate-700">
        {{ testimonial.text }}
      </div>
      <div class="flex items-center gap-2">
        <div class="w-8 h-8 bg-[#D9D9D9] rounded-full"></div>
        <span class="text-slate-700">{{ testimonial.author }}</span>
      </div>
    </div>
    <NuxtLink :to="url" target="_blank">Voir la version live ></NuxtLink>
  </div>
</template>
