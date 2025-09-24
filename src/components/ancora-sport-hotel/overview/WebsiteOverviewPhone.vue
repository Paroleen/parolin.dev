<script setup lang="ts">
import Homepage from "../../../assets/ancora-sport-hotel/homepage.png";
import EventDetails from "../../../assets/ancora-sport-hotel/event_details.png";
</script>

<template>
  <div class="relative rounded-t-4xl border border-white/10 bg-neutral-800/80">
    <div class="my-6 flex w-full items-center justify-center gap-2">
      <div class="h-2 w-2 rounded-full bg-white/10"></div>
      <div class="h-1 w-12 rounded-full bg-white/10"></div>
    </div>

    <div
      class="relative mx-5 overflow-hidden rounded-t-2xl max-[20em]:h-[300px] min-[20em]:max-[23em]:h-[380px] min-[23em]:max-[26em]:h-[450px] min-[26em]:max-[30em]:h-[550px] min-[30em]:h-[580px] sm:h-[580px] md:h-[620px] lg:h-[525px]"
      aria-hidden="true"
    >
      <img :src="Homepage" class="w-full animate-phone-navigation-1" />
      <img
        :src="EventDetails"
        class="absolute top-0 w-full animate-phone-navigation-2"
      />
    </div>
  </div>
</template>
