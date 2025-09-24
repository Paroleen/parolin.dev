<script setup lang="ts">
import ExternalLinkIcon from "../icons/ExternalLinkIcon.vue";
import LinkedInButton from "../common/LinkedInButton.vue";
import GitHubButton from "../common/GitHubButton.vue";
</script>

<template>
  <footer class="mx-auto w-full max-w-6xl px-6 py-4 md:px-8">
    <div class="flex flex-col items-center justify-between md:flex-row">
      <div
        class="mb-6 flex flex-col items-center justify-center gap-1 text-sm text-white/75 md:mb-0 md:flex-row"
      >
        <span>Matteo Parolin</span>
        <span class="hidden md:block" aria-hidden="true">|</span>
        <span>VAT Number: IT04344770245</span>
        <span class="hidden md:block" aria-hidden="true">|</span>
        <a
          href="https://github.com/Paroleen/parolin.dev"
          class="flex items-start gap-0.5 font-medium text-white"
        >
          Built with Vue.js
          <ExternalLinkIcon class="h-2.5 w-2.5" aria-hidden="true" />
        </a>
      </div>

      <div class="flex justify-around gap-1">
        <LinkedInButton />
        <GitHubButton />
      </div>
    </div>
  </footer>
</template>
