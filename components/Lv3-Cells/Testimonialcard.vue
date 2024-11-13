<template>
  <div class="testimonial-card">
    <div class="testimonial-card__image">
      <NuxtImg
        :src="imageSrc"
        alt="logo"
        class="testimonial-card__img h-11 w-11"
      />
    </div>
    <AzuraText tag="p" color="blue-horizon" size="lg" weight="normal">
      {{ description }}
    </AzuraText>
    <div class="testimonial-card__author">
      <div class="testimonial-card__image">
        <NuxtImg
          :src="photoSrc"
          alt="logo"
          class="testimonial-card__img h-14 w-14"
        />
      </div>
      <div class="testimonial-card__info">
        <AzuraText tag="p" color="navy" size="1.75rem" weight="semibold">
          {{ name }}
        </AzuraText>
        <AzuraText tag="p" color="blue-horizon" size="xl" weight="normal">
          {{ position }}
        </AzuraText>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
interface Props {
  imageSrc: string;
  description: string;
  photoSrc: string;
  name: string;
  position: string;
}
const props = defineProps<Props>();
</script>

<style scoped>
.testimonial-card {
  @apply bg-white py-8  px-4 flex flex-col gap-8 rounded-xl;
}
.testimonial-card__author {
  @apply flex flex-row gap-4 items-center;
}
</style>
