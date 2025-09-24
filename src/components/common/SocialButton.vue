<script setup lang="ts">
defineProps<{
  to: string;
  title: string;
}>();
</script>

<template>
  <a
    :href="to"
    :title="title"
    target="_blank"
    class="flex justify-center rounded-full p-2 hover:bg-neutral-800"
  >
    <div aria-hidden="true">
      <slot />
    </div>
  </a>
</template>
