<script setup lang="ts">
import FeatureCard from "../../common/FeatureCard.vue";
import HouseIcon from "../../icons/HouseIcon.vue";
import SearchIcon from "../../icons/SearchIcon.vue";
</script>

<template>
  <FeatureCard
    title="Find a property nearby"
    description="Use advanced filters to find the property that perfectly suits your needs."
  >
    <div class="relative flex w-fit flex-col items-center justify-center">
      <div class="absolute z-10 animate-magnifier text-neutral-100">
        <SearchIcon class="h-4 stroke-white" />
      </div>

      <div class="opacity-75">
        <HouseIcon class="h-6 stroke-[#858585]" />
      </div>
    </div>
  </FeatureCard>
</template>
