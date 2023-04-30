<script setup>
import { useMediaQuery } from "@vueuse/core";
const isLargeScreen = useMediaQuery("(min-width: 1024px)");
function setScreen() {
  return {isLargeScreen}
}
</script>

<template>
  <nav v-if="isLargeScreen">largeScren</nav>
  <nav v-else>smallScreen </nav>

  <header class="w-full flex text-center content-center justify-center">
    <video class="relative" autoplay loop muted>
      <source src="src/assets/шматки.mp4" type="video/webm" />
      <source src="src/assets/шматки.mp4" type="video/mp4" />
    </video>
    <img
      class="object-contain absolute mx-auto mt-[15%] inset-0 content-center"
      src="src/assets/VIKTORIIA POHRIBNA (1).png"
    />
  </header>
</template>
