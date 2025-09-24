<script setup lang="ts">
import Icon from "../assets/ancora-sport-hotel/logo.png";
import ProjectIcon from "./common/ProjectIcon.vue";
import HotelMapCard from "./ancora-sport-hotel/HotelMapCard.vue";
import AdminDashboardCard from "./ancora-sport-hotel/AdminDashboardCard.vue";
import WebsiteOverviewCard from "./ancora-sport-hotel/WebsiteOverviewCard.vue";
</script>

<template>
  <section class="flex flex-col items-center justify-center px-6 md:px-8">
    <ProjectIcon
      to="https://app.ancorasporthotel.it"
      title="Ancora Sport Hotel"
    >
      <img :src="Icon" class="z-10 ml-1 h-10 text-white" />
    </ProjectIcon>

    <p class="mt-6 mb-8 max-w-[50em] text-center text-sm text-white/75">
      Ancora Sport Hotel's event platform
      <span class="font-medium text-white"
        >offers guests and visitors an intuitive way to discover on-site and
        off-site activities</span
      >. From golf, tennis and padel lessons to yoga sessions, massages, themed
      dinners and aperitifs, explore detailed schedules at a glance. Seamlessly
      plan your next two weeks of exclusive wellness and sports with ease.
    </p>

    <div class="grid grid-cols-1 justify-center gap-6 lg:grid-cols-2">
      <div
        class="order-2 flex max-w-[30em] flex-col gap-6 text-sm text-white lg:order-1 lg:w-96"
      >
        <HotelMapCard class="order-2 lg:order-1" />
        <AdminDashboardCard class="order-1 lg:order-2" />
      </div>

      <WebsiteOverviewCard class="order-1 max-w-[30em] lg:w-96" />
    </div>
  </section>
</template>
