<script setup lang="ts">
import ExternalLinkIcon from "../icons/ExternalLinkIcon.vue";

defineProps<{
  to: string;
  title: string;
}>();
</script>

<template>
  <a
    :href="to"
    target="_blank"
    class="flex flex-col items-center justify-center"
  >
    <div class="flex h-12 w-12 items-center justify-center rounded-full">
      <div aria-hidden="true">
        <slot></slot>
      </div>

      <div
        class="absolute z-0 h-9 w-9 rounded-full bg-neutral-500/80 blur-xl"
      ></div>
    </div>

    <h2
      class="text-md flex items-start justify-center gap-1 font-medium tracking-tighter text-white"
    >
      {{ title }}
      <ExternalLinkIcon class="h-3 w-3" stroke-width="2.5" aria-hidden="true" />
    </h2>
  </a>
</template>
