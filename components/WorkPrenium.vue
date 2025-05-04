<script setup lang="ts">
const tag = `gallery`;
const title = `Mes derniers travaux`;
const text = `All the beautiful sites featured in the Framer Gallery\n are powered by Motion. Here are some more amazing\n interactions made by developers with its flexible APIs.`;
</script>

<template>
  <section
    id="work"
    class="pt-12 pb-20 md:pb-28 flex flex-col items-center gap-6"
  >
    <AnimatedText :animationDelay="0.5">
      <div class="uppercase text-xs bg-slate-200 px-3 py-1 rounded-full">
        {{ tag }}
      </div>
    </AnimatedText>
    <div class="flex flex-col gap-2">
      <h1
        class="text-xl md:text-2xl lg:text-3xl max-w-xl mx-auto animate-slide-up flex gap-1 flex-wrap"
      >
        <AnimatedText
          v-for="(word, wordIndex) in title.split(' ')"
          :animationDelay="wordIndex * 0.1"
        >
          {{ word }}
        </AnimatedText>
      </h1>
      <h1 class="text-md max-w-xl mx-auto flex justify-center flex-wrap">
        <AnimatedText
          v-for="(part, partIndex) in text.split('\n')"
          :animationDelay="0.5 + partIndex * 0.07"
        >
          {{ part }}
        </AnimatedText>
      </h1>
    </div>
  </section>
</template>
