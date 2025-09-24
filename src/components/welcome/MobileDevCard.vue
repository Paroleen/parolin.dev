<script setup lang="ts">
import Flutter from "../../assets/technologies/flutter.svg";
import AppStack from "./AppStack.vue";
</script>

<template>
  <div
    class="flex h-full w-full flex-col gap-4 text-white lg:h-80 lg:justify-between lg:gap-0"
  >
    <div class="w-full">
      <h2 class="text-center font-medium">Mobile app development</h2>
      <p class="text-center text-sm text-white/75">
        Custom mobile app development for iOS and Android, focusing on modern,
        reliable online and offline capabilities, push notification integration,
        in-app purchases and cross-platform consistency.
      </p>
    </div>

    <div class="relative flex h-52 w-full justify-center">
      <AppStack class="relative -top-8" aria-hidden="true" />

      <div
        class="absolute bottom-1 z-20 flex items-center gap-1 font-mono text-xs tracking-tight text-white/60 uppercase"
      >
        <img :src="Flutter" class="mb-1 h-3 grayscale" aria-hidden="true" />
        Flutter
      </div>
    </div>
  </div>
</template>
