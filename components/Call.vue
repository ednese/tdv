<script setup lang="ts"></script>

<template>
  <section class="pt-12 pb-20 md:pb-28">
    <div
      class="container bg-[#0D0D0D] mx-auto px-4 py-10 rounded-3xl text-center border-dashed border-2 border-slate-300 mx-auto max-w-(--breakpoint-xl)"
    >
      <h1
        class="uppercase text-xl md:text-2xl lg:text-3xl max-w-xl mx-auto font-bold mb-6 text-white animate-slide-up"
      >
        Planifiez un appel dès maintenant
      </h1>
      <p
        class="text-sm md:text-lg max-w-xl mx-auto mb-10 text-white animate-slide-up"
        style="animation-delay: 100ms"
      >
        Réservez un appel pour discuter de vos besoins et trouver la meilleure
        solution ensemble.
      </p>

      <NuxtLink
        to="https://cal.com/evansende/qualification-freelance?overlayCalendar=true"
        target="_blank"
        class="rounded-full bg-white btn-primary py-4 px-6 uppercase"
      >
        prendre un rendez-vous
      </NuxtLink>
    </div>

    <!-- <div
      style="width: 100%; height: 100%; overflow: scroll"
      id="my-cal-inline"
    ></div> -->
  </section>
</template>
