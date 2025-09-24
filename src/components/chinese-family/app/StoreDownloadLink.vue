<script setup lang="ts">
import ExternalLinkIcon from "../../icons/ExternalLinkIcon.vue";

defineProps<{
  to: string;
}>();
</script>

<template>
  <a
    :href="to"
    target="_blank"
    class="flex gap-0.5 text-xs font-bold text-white"
  >
    <div class="flex items-center gap-1">
      <slot />
    </div>

    <ExternalLinkIcon class="h-2 w-2" stroke-width="2.5" aria-hidden="true" />
  </a>
</template>
