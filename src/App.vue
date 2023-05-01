<script setup>
import { useMediaQuery } from "@vueuse/core";
const isLargeScreen = useMediaQuery("(min-width: 1024px)");
function setScreen() {
  return { isLargeScreen };
}
</script>

<template>
  <nav
    class="w-[100vw] top-0 left-0 fixed z-10 flex h-9 m-3 justify-around align-center h-11 p-11 text-xl text-white font-sf"
    v-if="isLargeScreen"
  >
    <a>Work</a>
    <a>Social</a>
    <a>Contact</a>
  </nav>
  <nav class="w-100 top-0 left-0 fixed z-10 flex h-9 m-3" v-else>
    <button class="text-white font-semibold ml-[18rem] right-0">MENU</button>
  </nav>

  <header class="w-full flex text-center content-center justify-center z-0 sm:h-full">
    <video class="relative sm:object-fill" autoplay loop muted>
      <source src="src/assets/шматки.mp4" type="video/webm" />
      <source src="src/assets/шматки.mp4" type="video/mp4" />
    </video>
    <img
      class="absolute mx-auto mt-[17%] inset-0 content-center"
      src="src/assets/VIKTORIIA POHRIBNA (1).png"
    />
  </header>

  <section class="w-full h-28 lg:flex lg:mt-16 ">
    <video class="relative lg:w-3/12 lg:ml-[8%] lg:mt-0 lg:h-60 sm:w-[80%]" autoplay loop muted>
      <source src="src/assets/hello.mp4" type="video/webm" />
      <source src="src/assets/hello.mp4" type="video/mp4" />
    </video>

    <div class="flex items-center justify-center content-center">
    <p class="text-2xl uppercase lg:text-6xl lg:mt-32 lg:ml-11 font-sf">
    I'm Viktoriia, a Ukrainian animator and illustrator based in Germany
    </p>
    </div>
  </section>
</template>
