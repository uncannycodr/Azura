<template>
  <div class="advanced-feature">
    <div class="advanced-feature__image">
      <NuxtImg :src="imageSrc" alt="logo" class="advanced-feature__img" />
    </div>
    <AzuraText tag="p" color="navy" size="2rem" weight="semibold">
      {{ title }}
    </AzuraText>
    <AzuraText tag="p" color="blue-horizon" size="xl" weight="normal">
      {{ description }}
    </AzuraText>
  </div>
</template>

<script setup lang="ts">
interface Props {
  imageSrc: string;
  title: string;
  description: string;
}

const props = defineProps<Props>();
</script>

<style scoped>
.advanced-feature {
  @apply flex flex-col  gap-2 py-[152px];
}

.advanced-feature__img {
  @apply w-[60px] h-[60px];
}
</style>
