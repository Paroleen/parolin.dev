<script setup lang="ts">
import FeatureCard from "../../common/FeatureCard.vue";
import TagIcon from "../../icons/TagIcon.vue";
</script>

<template>
  <FeatureCard
    title="Taggable events"
    description="Mark events as premium package inclusions."
  >
    <div class="relative flex h-6.5 w-fit items-center justify-center">
      <TagIcon class="z-10 w-4.5 fill-neutral-900" stroke-width="1.5" />
      <TagIcon class="absolute z-0 w-4.5 animate-tag" stroke-width="1.5" />
    </div>
  </FeatureCard>
</template>
