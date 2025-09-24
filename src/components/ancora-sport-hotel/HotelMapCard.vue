<script setup lang="ts">
import HotelMapPhone from "./map/HotelMapPhone.vue";
</script>

<template>
  <div
    class="relative flex flex-col items-center justify-center rounded-2xl bg-neutral-900 px-6 pb-6"
  >
    <div
      class="absolute top-0 z-10 h-20 w-full rounded-t-2xl bg-gradient-to-b from-neutral-900 to-transparent"
    ></div>

    <HotelMapPhone />

    <div class="mt-6 text-sm text-white">
      <h3 class="font-bold">Find your next event</h3>

      <p class="text-white/75">
        Locate events within Ancora Sport Hotel on a detailed interactive map
        and explore all on-site venues for easy navigation.
      </p>
    </div>
  </div>
</template>
