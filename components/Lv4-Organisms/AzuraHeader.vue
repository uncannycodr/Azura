<template>
  <!-- Default Header (Visible at the top) -->
  <div v-show="!isScrolled" class="header1">
    <div class="header1__image">
      <NuxtImg
        src="/images/logo.png"
        alt="logo"
        class="header1__img w-32 h-10"
      />
    </div>
    <AzuraMenu :class="{ hidden: !isMenuOpen }" />
    <div class="hidden lg:block">
      <AzuraButton as="button" variant="outline" class="bg-white">
        <AzuraText tag="p" color="navy" size="base" weight="semibold"
          >Contact Us</AzuraText
        >
      </AzuraButton>
    </div>

    <div class="flex lg:hidden">
      <AzuraButton as="button">
        <component
          :is="isMenuOpen ? IconX : IconAlignLeft"
          class="h-6 w-6 text-black"
        />
      </AzuraButton>
    </div>
  </div>

  <!-- Fixed Centered Header (Appears on scroll down) -->
  <div
    v-show="isScrolled"
    class="header2-container fixed top-8 w-full lg:flex justify-center hidden"
  >
    <div
      class="header2 bg-white rounded-full px-4 py-2 flex flex-row items-center shadow-lg"
    >
      <div class="header2__image">
        <NuxtImg
          src="/images/logo.png"
          alt="logo"
          class="header2__img w-32 h-10"
        />
      </div>
      <AzuraMenu />
      <AzuraButton as="button" variant="outline" class="bg-white">
        <AzuraText tag="p" color="navy" size="base" weight="semibold"
          >Contact Us</AzuraText
        >
      </AzuraButton>
    </div>
  </div>
</template>

<script setup lang="ts">
import { IconAlignLeft, IconX } from "@tabler/icons-vue";

import { onMounted, onUnmounted, ref } from "vue";

const isMenuOpen = ref(false);
const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value;
};
const isScrolled = ref(false);

const handleScroll = () => {
  // Show header2 after scrolling 50px down
  isScrolled.value = window.scrollY > 50;
};

onMounted(() => {
  window.addEventListener("scroll", handleScroll);
});

onUnmounted(() => {
  window.removeEventListener("scroll", handleScroll);
});
</script>

<style scoped>
.header1 {
  @apply max-w-[1312px] px-6 mx-auto mt-6 flex flex-row items-center justify-between;
}
.header2-container {
  z-index: 50; /* Ensures header2 is on top */
}
.header2 {
  @apply max-w-[800px] flex items-center justify-center gap-20;
}
</style>
