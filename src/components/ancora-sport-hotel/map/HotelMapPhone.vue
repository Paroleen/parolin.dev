<script setup lang="ts">
import Map from "../../../assets/ancora-sport-hotel/map.png";
</script>

<template>
  <div
    class="relative flex w-full items-end justify-center overflow-hidden rounded-b-4xl border-r border-b border-l border-white/10 bg-neutral-800/80 lg:h-55"
  >
    <div
      class="mx-5 mb-5 flex h-full w-full justify-center overflow-hidden rounded-b-2xl"
    >
      <img
        :src="Map"
        class="animate-map object-cover opacity-75"
        aria-hidden="true"
      />
    </div>

    <div class="absolute flex justify-center">
      <div class="z-10 my-2 h-1 w-26 rounded-xl bg-white/10"></div>
    </div>
  </div>
</template>
