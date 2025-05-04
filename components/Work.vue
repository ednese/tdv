<script setup lang="ts">
import { NuxtLink } from "#components";
const companies = [
  {
    logo: "/img/work_logos/ca.jpg",
    name: "Crédit Agricole",
    text: "J'ai conçu et développé des interfaces graphiques pour des solutions d'IA générative. Mon rôle a été d'améliorer les interfaces existantes en garantissant performance et qualité, d'assurer le déploiement sur AWS via GitLab CI/CD et de rédiger une documentation technique claire.",
    skills: [
      "Front End",
      "Nuxt / Vue",
      "Design",
      "Tests unitaires",
      "Typescript",
      "AWS",
      "GitLab CI/CD",
    ],
    testimonial: {
      text: "Lorem Ipsum is simply dummy text of the printing and typesetting industry. Lorem Ipsum has been the industry's standard dummy text ever since the 1500s, when an unknown printer took a galley of type and scrambled it to make a type specimen book.",
      author: "Vincent C. - Développeur Front End Senior",
    },
    url: "https://www.credit-agricole.fr/",
    image: "/img/work_image_placeholder.png",
  },
  {
    logo: "/img/work_logos/bm.jpg",
    name: "BackMarket",
    text: "J'ai contribué à la migration du site vers Nuxt 3, améliorant ainsi sa performance et sa maintenabilité. J'ai mis en place des tests unitaires et E2E pour garantir la fiabilité du code et participé à l'optimisation des nouvelles pages, notamment celles dédiées au recyclage, utilisées par plus de 6 000 clients.",
    skills: ["Front End", "Nuxt / Vue", "Typescript", "Tests unitaires"],
    testimonial: {
      text: "Toujours à l'écoute et force de proposition, il possède des connaissances techniques solides et n'hésite pas à challenger les choix techniques pour toujours trouver la meilleure solution.Je le recommande sans hésiter pour n'importe quel projet !",
      author: "Said K. - Développeur Front End Senior",
    },
    url: "https://backmarket.fr",
    image: "/img/work_image_placeholder.png",
  },
  {
    logo: "/img/work_logos/fifteen.jpg",
    name: "Fifteen",
    text: "J'ai travaillé sur la refonte du site fifteen.eu en Vue/Nuxt 3, en mettant l'accent sur la performance web et le SEO. J'ai également développé une librairie de composants réutilisables avec Storybook et intégré un blog sous Strapi pour améliorer le référencement naturel et l'engagement des utilisateurs.",
    skills: ["Front End", "Nuxt / Vue", "Typescript", "Tests unitaires"],
    testimonial: {
      text: "Travailler avec Evan a été une expérience enrichissante. Il a beaucoup appris de cette mission et s'est montré rigoureux, réfléchi, organisé, et force de propositions et d'initiatives. Il est passionné par la technologie, possède une compréhension aiguisée du design et sera sans aucun doute un atout pour votre équipe.",
      author: "François R. - Head of Front End Development",
    },
    url: "https://fifteen.eu/",
    image: "/img/work_image_placeholder.png",
  },
];
</script>

<template>
  <section id="work" class="pt-12 pb-20 md:pb-28">
    <div
      class="container bg-[#F5F5F5] mx-auto px-4 py-10 rounded-3xl text-center border-dashed border-2 border-slate-300 mx-auto max-w-(--breakpoint-xl)"
    >
      <h1
        class="text-xl md:text-2xl lg:text-3xl max-w-xl mx-auto font-bold mb-6 animate-slide-up"
      >
        CE QUE J'AI APPORTÉ DANS "DIFFÉRENTS TYPES" DE BOITES
      </h1>
      <p
        class="text-sm md:text-lg max-w-xl mx-auto mb-10 text-gray-600 animate-slide-up"
        style="animation-delay: 100ms"
      >
        Avec une expérience dans divers secteurs et des solutions adaptées à
        chaque projet, je développe des interfaces qui font la différence.
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
      </div>
      <div class="mt-12 flex flex-col gap-8">
        <div
          v-for="(company, index) in companies"
          class="flex flex-1 flex-col xl:flex-row gap-10 items-center justify-center"
          :key="company.name"
        >
          <Company
            :class="{ 'xl:order-last': index % 2 === 1 }"
            :="company"
          ></Company>
          <img
            :src="company.image"
            :alt="company.image"
            class="max-h-fit"
            width="584"
            height="348"
          />
        </div>
      </div>
    </div>
  </section>
</template>
