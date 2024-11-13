<template>
  <div class="feature-images">
    <div class="feature-images__top">
      <FeatureImage />
      <FeatureImage />
    </div>

    <div class="feature-images__bottom">
      <FeatureImage />
      <FeatureImage />
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.feature-images {
  @apply flex flex-col gap-4;
}
.feature-images__top {
  @apply flex flex-row gap-4;
}
.feature-images__bottom {
  @apply flex flex-row gap-4;
}
</style>
