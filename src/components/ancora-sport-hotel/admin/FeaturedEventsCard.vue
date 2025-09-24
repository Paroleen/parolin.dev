<script setup lang="ts">
import FeatureCard from "../../common/FeatureCard.vue";
import ChevronsUpIcon from "../../icons/ChevronsUpIcon.vue";
</script>

<template>
  <FeatureCard
    title="Featured section"
    description="Spotlight important events by placing them in the featured section."
  >
    <div class="flex h-6.5 w-fit items-center justify-center">
      <ChevronsUpIcon class="w-5 animate-chevron-up" stroke-width="1.5" />
    </div>
  </FeatureCard>
</template>
