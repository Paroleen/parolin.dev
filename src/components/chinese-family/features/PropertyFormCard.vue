<script setup lang="ts">
import FeatureCard from "../../common/FeatureCard.vue";
import PlusIcon from "../../icons/PlusIcon.vue";
</script>

<template>
  <FeatureCard
    title="Add a property easily"
    description="List your real estate with the intuitive step-by-step submission form."
  >
    <div class="flex h-6.5 w-fit items-center justify-center">
      <PlusIcon class="w-5 animate-plus" stroke-width="1.5" />
    </div>
  </FeatureCard>
</template>
