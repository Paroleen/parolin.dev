<script setup lang="ts">
import AppStoreIcon from "../icons/AppStoreIcon.vue";
import PlayStore from "../icons/PlayStoreIcon.vue";
import AppLink from "./app/StoreDownloadLink.vue";
</script>

<template>
  <div class="max-w-[30em] rounded-2xl bg-[#171717] p-6 text-sm">
    <h3 class="font-bold text-white">
      The Chinese Family app is now available
    </h3>

    <p class="text-white/75">
      Browse, buy, sell or rent Italian properties anywhere, anytime. Download
      the app today!
    </p>

    <div class="mt-4 flex gap-4">
      <AppLink
        to="https://play.google.com/store/apps/details?id=it.chinesefamily.app&hl=en-US"
      >
        <PlayStore class="h-3.5 fill-white" aria-hidden="true" />
        Play Store
      </AppLink>

      <AppLink to="https://apps.apple.com/us/app/chinese-family/id1587917957">
        <AppStoreIcon class="h-4.5 fill-white" aria-hidden="true" />
        App Store
      </AppLink>
    </div>
  </div>
</template>
