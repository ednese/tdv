<script setup lang="ts">
import { NuxtLink } from "#components";
const logos = ["matchem", "ca", "backmarket", "fifteen", "askup"];
</script>

<template>
  <section class="pt-12 pb-20 md:pb-28">
    <div
      class="container bg-white mx-auto px-4 py-10 rounded-3xl text-center border-dashed border-2 border-slate-300 mx-auto max-w-screen-xl"
    >
      <h1
        class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 animate-slide-up"
      >
        Développeur expert pour<br />
        des interfaces performantes<br />
        et évolutives
      </h1>
      <p
        class="text-lg md:text-xl max-w-3xl mx-auto mb-10 text-gray-600 animate-slide-up"
        style="animation-delay: 100ms"
      >
        Avec plus de 4 ans d’expérience auprès de startups et grands groupes, je
        conçois et développe des interfaces graphiques sur mesure, alliant
        performance, scalabilité et expérience utilisateur optimale.
      </p>
      <div
        class="flex flex-col sm:flex-row justify-center gap-12 animate-slide-up"
        style="animation-delay: 200ms"
      >
        <NuxtLink
          to="https://cal.com/evansende/qualification-freelance?overlayCalendar=true"
          target="_blank"
          class="rounded-full bg-black text-white btn-primary py-4 px-6 uppercase"
        >
          prendre un rendez-vous
        </NuxtLink>
        <NuxtLink
          to="#work"
          class="rounded-full border-solid border-2 border-slate-200 btn-primary py-4 px-6 uppercase"
        >
          mes expériences
        </NuxtLink>
      </div>
      <div
        class="mx-auto mt-16 max-w-2xl text-start bg-[#F0F0F0] p-4 rounded-xl flex flex-col gap-4"
      >
        <div>
          J'ai eu le plaisir de travailler avec Evan sur la partie front de
          ParisTurf, je le recommande les yeux fermés. Il est techniquement
          solide, fiable et ultra investi, c'est exactement le genre de
          développeur "A-player" qu'on veut avoir dans son équipe. Au plaisir de
          remettre ça sur une prochaine mission !
        </div>
        <div class="flex items-center gap-2">
          <div class="w-8 h-8 bg-[#D9D9D9] rounded-full"></div>
          <span>Alexandre S.</span>
        </div>
      </div>
      <p class="mt-16">
        Ils m’ont fait confiance pour passer à la vitesse supérieur.
      </p>
      <div class="flex flex-col xl:flex-row gap-12 mx-auto w-fit mt-8">
        <img
          v-for="logo in logos"
          :src="`/img/header_logos/${logo}.svg`"
          :alt="logo"
          height="40"
        />
      </div>
    </div>
  </section>
</template>
