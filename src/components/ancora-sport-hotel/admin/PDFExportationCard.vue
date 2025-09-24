<script setup lang="ts">
import FeatureCard from "../../common/FeatureCard.vue";
import DownloadIcon from "../../icons/DownloadIcon.vue";
</script>

<template>
  <FeatureCard
    title="PDF exportation"
    description="Export event lists as PDF documents for offline distribution."
  >
    <div class="flex h-6.5 w-fit items-center justify-center">
      <DownloadIcon class="w-4.5" stroke-width="1.5" />
    </div>
  </FeatureCard>
</template>
