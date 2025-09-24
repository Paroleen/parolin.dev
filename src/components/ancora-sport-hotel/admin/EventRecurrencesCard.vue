<script setup lang="ts">
import FeatureCard from "../../common/FeatureCard.vue";
import CalendarSyncIcon from "../../icons/CalendarSyncIcon.vue";
</script>

<template>
  <FeatureCard
    title="Event recurrences"
    description="Schedule events to repeat daily, weekly, monthly or yearly."
  >
    <div class="flex h-6.5 w-fit items-center justify-center">
      <CalendarSyncIcon class="w-4.5" stroke-width="1.5" />
    </div>
  </FeatureCard>
</template>
