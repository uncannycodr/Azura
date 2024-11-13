<template>
  <div class="hero-section">
    <HeroTop />
    <HeroBottom />
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.hero-section {
  @apply max-w-[1312px] mx-auto flex flex-col gap-20 items-center py-24;
}
</style>
