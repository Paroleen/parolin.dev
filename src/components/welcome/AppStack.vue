<script setup lang="ts">
import CircleAppIcon from "../../assets/icons/circle_app_icon.svg";
import SquareAppIcon from "../../assets/icons/square_app_icon.svg";
import TriangleAppIcon from "../../assets/icons/triangle_app_icon.svg";
</script>

<template>
  <div
    class="flex h-full w-full items-center justify-center perspective-[2000px] perspective-origin-[50%]"
  >
    <img :src="CircleAppIcon" class="z-10 h-20 animate-circle-app" />
    <img :src="SquareAppIcon" class="absolute z-5 h-20 animate-square-app" />
    <img :src="TriangleAppIcon" class="absolute h-20 animate-triangle-app" />
  </div>
</template>
