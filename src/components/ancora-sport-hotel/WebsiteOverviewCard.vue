<script setup lang="ts">
import WebsiteOverviewPhone from "./overview/WebsiteOverviewPhone.vue";
</script>

<template>
  <div
    class="relative flex flex-col items-center justify-center rounded-2xl bg-neutral-900 px-6 pt-6 text-sm text-white"
  >
    <div class="mb-6 text-sm text-white">
      <h3 class="font-bold">Plan your vacation</h3>

      <p class="text-white/75">
        After registering, users can browse and filter all upcoming hotel events
        and external activities scheduled within the next two weeks, with event
        details available in both English and Italian.
      </p>
    </div>

    <WebsiteOverviewPhone />

    <div
      class="absolute bottom-0 left-0 h-20 w-full rounded-b-2xl bg-gradient-to-b from-transparent to-neutral-900"
    ></div>
  </div>
</template>
