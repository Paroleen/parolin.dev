<script setup lang="ts">
import LaptopFace from "../../assets/emojis/laptop.png";
import LinkedInButton from "../common/LinkedInButton.vue";
import GitHubButton from "../common/GitHubButton.vue";
</script>

<template>
  <nav
    class="mx-2 flex h-12 w-96 animate-navbar items-center justify-between rounded-full bg-neutral-900/70 px-4 shadow-[inset_1px_0_#ffffff0a,_inset_-1px_0_#ffffff0a,_inset_0_1px_#ffffff1a,_inset_0_1px_#ffffff1a] backdrop-blur-sm"
  >
    <div class="flex items-center gap-1">
      <img
        class="h-8 w-8"
        :src="LaptopFace"
        alt="Matteo Parolin emoji typing on a laptop"
      />

      <div class="flex flex-col text-white">
        <h1 class="text-sm font-medium tracking-tight">Matteo Parolin</h1>
        <h2 class="text-xs font-light">Freelance software engineer</h2>
      </div>
    </div>

    <div class="flex items-center gap-1">
      <LinkedInButton />
      <GitHubButton />
    </div>
  </nav>
</template>
