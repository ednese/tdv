<script setup lang="ts">
import { motion } from "motion-v";

const props = withDefaults(
  defineProps<{
    animationDelay?: number;
    type?: "default" | "blur";
  }>(),
  {
    animationDelay: 0,
    type: "default",
  }
);

const divProps = computed(() => {
  const baseProps = {
    initial: { opacity: 0, y: 10 },
    "while-in-view": { opacity: 1, y: 0 },
    transition: { duration: 0.7, delay: props.animationDelay },
    "in-view-options": { once: true },
  };

  if (props.type === "blur") {
    return {
      ...baseProps,
      initial: { ...baseProps["initial"], filter: "blur(6px)" },
      "while-in-view": { ...baseProps["while-in-view"], filter: "blur(0px)" },
    };
  }

  return baseProps;
});
</script>

<template>
  <motion.div :="divProps">
    <slot />
  </motion.div>
</template>
