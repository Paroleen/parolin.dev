<script setup lang="ts">
import SmilingEmoji from "../assets/emojis/smiling.png";
import LinkedInButton from "./common/LinkedInButton.vue";
import GitHubButton from "./common/GitHubButton.vue";
import FullstackDevCard from "./welcome/FullstackDevCard.vue";
import MobileDevCard from "./welcome/MobileDevCard.vue";
</script>

<template>
  <section class="flex w-full flex-col items-center px-6 md:px-8 lg:max-w-6xl">
    <div class="mt-6 mb-16 flex flex-col items-center justify-center">
      <img :src="SmilingEmoji" class="mb-4 h-32" alt="Matteo Parolin emoji" />

      <h1 class="text-center text-2xl font-bold tracking-tighter text-white">
        Matteo Parolin
      </h1>
      <p class="text-center text-sm font-medium tracking-tight text-white/75">
        Freelance software engineer
      </p>

      <div class="mt-2 flex gap-2">
        <LinkedInButton />
        <GitHubButton />
      </div>
    </div>

    <div
      class="flex w-full max-w-[31em] flex-col items-center justify-center gap-16 lg:max-w-full lg:flex-row lg:gap-12 xl:gap-16"
    >
      <FullstackDevCard class="lg:h-80" />
      <MobileDevCard class="lg:h-80" />
    </div>
  </section>
</template>
