<script setup lang="ts">
import FeaturedEventsCard from "./admin/FeaturedEventsCard.vue";
import EventRecurrencesCard from "./admin/EventRecurrencesCard.vue";
import PDFExportationCard from "./admin/PDFExportationCard.vue";
import TaggableEventsCard from "./admin/TaggableEventsCard.vue";
</script>

<template>
  <div
    class="flex h-full flex-col justify-between rounded-xl bg-neutral-900 p-6"
  >
    <div class="text-sm text-white">
      <h3 class="font-bold">Manage the events seamlessly</h3>

      <p class="text-white/75">
        Administrators can create, edit and publish events with ease from the
        dedicated dashboard.
      </p>
    </div>

    <div
      class="mt-6 grid grid-cols-2 gap-4"
      aria-label="Admin dashboard features"
    >
      <FeaturedEventsCard />
      <EventRecurrencesCard />
      <PDFExportationCard />
      <TaggableEventsCard />
    </div>
  </div>
</template>
