<script setup lang="ts">
import WebBrowser from "./chinese-family/WebBrowserSlideshow.vue";
import ChineseFamilyIcon from "./icons/ChineseFamilyIcon.vue";
import AppCard from "./chinese-family/AppDownloadCard.vue";
import ProjectIcon from "./common/ProjectIcon.vue";
import AddPropertyCard from "./chinese-family/features/PropertyFormCard.vue";
import TranslationRequestCard from "./chinese-family/features/TranslationRequestCard.vue";
import PropertyPromotionCard from "./chinese-family/features/PropertyPromotionCard.vue";
import SearchPropertyCard from "./chinese-family/features/PropertySearchCard.vue";
</script>

<template>
  <section class="flex max-w-4xl flex-col items-center px-6 md:px-8">
    <ProjectIcon to="https://chinesefamily.it" title="Chinese Family">
      <ChineseFamilyIcon class="z-10 ml-1 h-8 text-white" />
    </ProjectIcon>

    <p class="mt-6 mb-8 max-w-[50em] text-center text-sm text-white/75">
      Discover Chinese Family,
      <span class="font-medium text-white"
        >a bilingual real estate platform connecting Italian and Chinese
        community members</span
      >
      for buying, selling or renting properties across Italy. With advanced
      search filters for region, size, price and more, Italian-Chinese
      interface, professional translation services, integrated messaging,
      personalized profiles and transparent reviews, Chinese Family ensures an
      efficient and tailored property experience.
    </p>

    <WebBrowser />

    <div class="my-8 grid grid-cols-2 gap-8 md:grid-cols-4">
      <AddPropertyCard />
      <TranslationRequestCard />
      <PropertyPromotionCard />
      <SearchPropertyCard />
    </div>

    <AppCard />
  </section>
</template>
