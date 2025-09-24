<script setup lang="ts">
defineProps<{
  title: string;
  description: string;
}>();
</script>

<template>
  <div class="text-sm text-white">
    <div aria-hidden="true">
      <slot></slot>
    </div>

    <h3 class="font-bold">{{ title }}</h3>
    <p class="text-white/75">
      {{ description }}
    </p>
  </div>
</template>
