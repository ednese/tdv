<template>
  <div>
    <NuxtPage />
  </div>
</template>

<script setup lang="ts">
useHead({
  script: [
    {
      src: "https://app.cal.com/embed/embed.js",
      async: true,
      onload: () => {
        // Initialize Cal after the script has loaded
        if (window.Cal) {
          window.Cal("init", "qualification-freelance", {
            origin: "https://cal.com",
          });

          window.Cal.ns["qualification-freelance"]("inline", {
            elementOrSelector: "#my-cal-inline",
            config: { layout: "month_view", theme: "dark" },
            calLink: "evansende/qualification-freelance",
          });

          window.Cal.ns["qualification-freelance"]("ui", {
            theme: "dark",
            hideEventTypeDetails: false,
            layout: "week_view",
          });
        } else {
          console.error("Cal is not defined after script load.");
        }
      },
    },
  ],
});
</script>
