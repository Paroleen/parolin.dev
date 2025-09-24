<script setup lang="ts">
import Homepage from "../../assets/chinese-family/homepage.png";
import PropertyDetails from "../../assets/chinese-family/property_details.png";
import PropertyCreation from "../../assets/chinese-family/property_creation.png";
import { onMounted, onUnmounted, ref, useTemplateRef } from "vue";
import LockIcon from "../icons/LockIcon.vue";
import ChevronLeftIcon from "../icons/ChevronLeftIcon.vue";
import ChevronRightIcon from "../icons/ChevronRightIcon.vue";
import ChineseFamilyIcon from "../icons/ChineseFamilyIcon.vue";

const tabs = [
  { title: "Properties in Padua", image: Homepage },
  { title: "Apartment in Via Roma, Padua", image: PropertyDetails },
  { title: "Edit property", image: PropertyCreation },
];
let timeoutId: number | null = null;
const currentTab = ref(0);

const tabsContainer = useTemplateRef("tabs-container");
const loadingBarDesktop = useTemplateRef("loading-bar-desktop");
const loadingBarMobile = useTemplateRef("loading-bar-mobile");

onMounted(() => {
  handleTabChange(0);

  window.addEventListener("resize", handleResize);
});

onUnmounted(() => {
  window.removeEventListener("resize", handleResize);

  if (timeoutId) {
    clearTimeout(timeoutId);
  }
});

function handleTimeout() {
  timeoutId = setTimeout(() => {
    const tab = (currentTab.value + 1) % tabs.length;

    handleTabChange(tab);
  }, 10000);
}

function handleResize() {
  disableSlideshowAnimation();
  updateSlideshow();
}

function handlePreviousTab() {
  handleTabChange(currentTab.value - 1);
}

function handleNextTab() {
  handleTabChange((currentTab.value + 1) % tabs.length);
}

function handleTabChange(tab: number) {
  if (timeoutId) {
    clearTimeout(timeoutId);
  }

  currentTab.value = tab;

  enableSlideshowAnimation();
  updateSlideshow();
  handleTimeout();
}

function updateSlideshow() {
  resetLoadingBar(loadingBarDesktop.value!);
  resetLoadingBar(loadingBarMobile.value!);

  const offset = currentTab.value * tabsContainer.value!.offsetWidth;
  tabsContainer.value!.style.transform = `translateX(-${offset}px)`;

  fillLoadingBar(loadingBarDesktop.value!);
  fillLoadingBar(loadingBarMobile.value!);
}

function enableSlideshowAnimation() {
  tabsContainer.value!.style.transition = "transform 0.5s ease";
}

function disableSlideshowAnimation() {
  tabsContainer.value!.style.transition = "";
}

function resetLoadingBar(loadingBar: HTMLDivElement) {
  loadingBar.style.transition = "";
  loadingBar.style.width = "0%";
}

function fillLoadingBar(loadingBar: HTMLDivElement) {
  loadingBar.style.transition = "width 10s linear";
  loadingBar.style.width = "100%";
}
</script>

<template>
  <div class="relative" aria-hidden="true">
    <div class="w-full">
      <div class="rounded-2xl border border-white/10">
        <div class="rounded-t-2xl bg-neutral-900">
          <div class="flex justify-between gap-3 px-2 py-1.5 md:gap-24 md:py-0">
            <div class="ml-1 flex gap-2 md:ml-4 md:gap-3">
              <button
                :class="[
                  currentTab > 0 ? 'cursor-pointer' : 'cursor-not-allowed',
                ]"
                tabindex="-1"
                @click="handlePreviousTab"
              >
                <ChevronLeftIcon
                  class="w-5 md:w-7"
                  :class="[
                    currentTab > 0 ? 'stroke-white/60' : 'stroke-white/10',
                  ]"
                />
              </button>
              <button
                :class="[
                  currentTab < tabs.length - 1
                    ? 'cursor-pointer'
                    : 'cursor-not-allowed',
                ]"
                tabindex="-1"
                @click="handleNextTab"
              >
                <ChevronRightIcon
                  class="w-5 md:w-7"
                  :class="[
                    currentTab < tabs.length - 1
                      ? 'stroke-white/60'
                      : 'stroke-white/10',
                  ]"
                />
              </button>
            </div>

            <a
              href="https://chinesefamily.it"
              target="_blank"
              class="relative m-3 hidden flex-grow overflow-hidden rounded-xl border border-white/10 md:block"
              tabindex="-1"
            >
              <div
                class="z-10 m-2 flex items-center gap-2 text-xs font-medium text-white/60"
              >
                <LockIcon class="w-3" stroke-width="3" />
                https://chinesefamily.it
              </div>

              <div
                class="absolute top-0 h-full bg-white/5"
                ref="loading-bar-desktop"
              ></div>
            </a>

            <div class="mr-3 flex items-center justify-end gap-2 md:mr-5">
              <div
                class="h-2 w-2 cursor-not-allowed rounded-full bg-white/10 md:h-2.5 md:w-2.5"
              ></div>
              <div
                class="h-2 w-2 cursor-not-allowed rounded-full bg-white/10 md:h-2.5 md:w-2.5"
              ></div>
              <div
                class="h-2 w-2 cursor-not-allowed rounded-full bg-white/10 md:h-2.5 md:w-2.5"
              ></div>
            </div>
          </div>

          <div class="hidden grid-cols-3 md:grid">
            <button
              v-for="(tab, index) in tabs"
              :key="index"
              class="flex cursor-pointer justify-center gap-1.5 border-t px-5 py-2 text-xs transition-all duration-250 ease-linear"
              :class="[
                currentTab === index
                  ? 'border-neutral-900 text-white'
                  : 'border-white/10 text-white/60',
                currentTab === 0 && index === 1 ? 'rounded-tl-md border-x' : '',
                currentTab === 1 && index === 0 ? 'rounded-tr-md border-r' : '',
                currentTab === 1 && index === 2 ? 'rounded-tl-md border-l' : '',
                currentTab === 2 && index === 1 ? 'rounded-tr-md border-x' : '',
              ]"
              tabindex="-1"
              @click="() => handleTabChange(index)"
            >
              <ChineseFamilyIcon class="w-3" />
              <span class="truncate">{{ tab.title }} | Chinese Family</span>
            </button>
          </div>

          <div class="h-0.75 bg-neutral-900 md:hidden">
            <div class="h-full bg-[#696969]" ref="loading-bar-mobile"></div>
          </div>
        </div>

        <div class="relative overflow-hidden rounded-b-2xl">
          <div class="flex" ref="tabs-container">
            <img
              v-for="(tab, index) in tabs"
              :key="index"
              :src="tab.image"
              class="w-full flex-shrink-0 object-cover opacity-90"
            />
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
