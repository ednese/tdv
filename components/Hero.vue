<script setup lang="ts">
import { NuxtLink } from "#components";
import { motion } from "motion-v";

const logos = ["paris_turf", "credit_agricole", "back_market", "fifteen"];
const headerTitle = "Frontend & Design selon vos enjeux.";
const headerText =
  "Développeur front-end avec un fort intérêt pour le design, j'interviens sur des projets variés, de startup à grand groupe.";
</script>

<template>
  <section class="pt-20 px-4 text-white flex flex-col items-center">
    <AnimatedText
      class="flex items-center gap-x-1"
      :animationDelay="0.5"
      type="blur"
    >
      <img
        src="/img/logo_white_laurel_crown.png"
        class="w-6 rotate-x-30 rotate-15"
      />
      <NuxtLink
        to="https://www.malt.fr/profile/evansende"
        target="_blank"
        class="font-semibold px-4 py-1 bg-slate-800 rounded-full flex items-center h-fit gap-x-3"
      >
        Super Malter
        <div class="flex gap-x-2">
          <img v-for="_ in 2" src="/img/super_malter.svg" class="w-3" />
        </div>
      </NuxtLink>
      <img
        src="/img/logo_white_laurel_crown.png"
        class="w-6 rotate-y-180 rotate-x-30 -rotate-15"
      />
    </AnimatedText>
    <h1
      class="flex flex-wrap justify-center gap-x-1 sm:gap-x-2 text-3xl sm:text-5xl lg:text-7xl font-medium text-blue-100 max-w-lg lg:max-w-xl mt-8"
    >
      <AnimatedText
        v-for="(word, wordIndex) in headerTitle.split(' ')"
        :animationDelay="wordIndex * 0.1"
        type="blur"
      >
        {{ word }}
      </AnimatedText>
    </h1>
    <h3
      class="mt-4 sm:mt-8 flex flex-wrap justify-center gap-x-1 text-sm sm:text-xl max-w-md sm:max-w-xl text-slate-400"
    >
      <AnimatedText
        v-for="(word, wordIndex) in headerText.split(' ')"
        :animationDelay="0.3 + wordIndex * 0.05"
        type="blur"
      >
        {{ word }}
      </AnimatedText>
    </h3>

    <div
      class="flex flex-col items-center sm:flex-row gap-2 mt-8"
      :animationDelay="1"
      type="blur"
    >
      <AnimatedText :animationDelay="1" type="blur">
        <NuxtLink
          to="https://cal.com/evansende/qualification-freelance?overlayCalendar=true&duration=15"
          target="_blank"
          class="uppercase px-5 py-3 bg-slate-200 text-sm rounded-full flex items-center h-fit text-black"
        >
          prendre un rendez-vous
        </NuxtLink></AnimatedText
      >
      <AnimatedText :animationDelay="1.1" type="blur">
        <NuxtLink
          to="https://www.linkedin.com/in/evan-sende"
          target="_blank"
          class="uppercase px-5 py-3 bg-slate-800 text-sm rounded-full flex items-center h-fit w-fit"
          >mon parcours</NuxtLink
        ></AnimatedText
      >
    </div>
    <div class="mt-12 flex flex-col items-center gap-y-4 text-blue-100">
      <AnimatedText :animationDelay="1.2" type="blur">
        <p>Ils m’ont fait confiance:</p>
      </AnimatedText>
      <div
        class="flex flex-col lg:flex-row gap-12 mx-auto w-fit justify-center items-center"
      >
        <AnimatedText
          v-for="(logo, logoIndex) in logos"
          :animationDelay="1.3 + logoIndex * 0.05"
          type="blur"
        >
          <img
            :src="`/img/header_logos/${logo}.svg`"
            :alt="logo"
            class="w-40"
          />
        </AnimatedText>
      </div>
    </div>
  </section>
</template>
