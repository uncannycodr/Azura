<template>
  <div class="feature-image">
    <div class="feature-image__image">
      <NuxtImg
        src="/images/image1.png"
        alt="logo"
        class="feature-image__img w-64"
      />
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.feature-image {
  @apply bg-chef-hat flex flex-col items-center px-4 pt-8 rounded-xl;
}
</style>
