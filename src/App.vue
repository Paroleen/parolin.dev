<script setup lang="ts">
import WelcomeSection from "./components/WelcomeSection.vue";
import ChineseFamilySection from "./components/ChineseFamilySection.vue";
import AncoraSportHotelSection from "./components/AncoraSportHotelSection.vue";
import Navbar from "./components/layout/Navbar.vue";
import Footer from "./components/layout/Footer.vue";
</script>

<template>
  <header class="sticky top-0 z-50 flex w-full justify-center pt-2 md:pt-4">
    <Navbar />
  </header>

  <main class="flex animate-content flex-col items-center gap-20 py-12">
    <WelcomeSection />
    <ChineseFamilySection />
    <AncoraSportHotelSection />
  </main>

  <Footer />
</template>
