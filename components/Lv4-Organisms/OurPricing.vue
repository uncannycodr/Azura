<template>
  <div class="our-pricing">
    <div class="our-pricing__text">
      <AzuraText
        tag="p"
        color="navy"
        size="5xl"
        weight="semibold"
        class="leading-[64px]"
      >
        Our Pricing
      </AzuraText>
      <AzuraText tag="p" color="navy" size="xl" weight="normal">
        Hear from satisfied clients who have transformed their property
        management experience with our platform.
      </AzuraText>
    </div>
    <div class="our-pricing__plans">
      <StarterPlan />
      <ProPlan />
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.our-pricing {
  @apply px-4 flex flex-col gap-20 py-28;
}
.our-pricing__text {
  @apply max-w-[615px] mx-auto items-center text-center flex flex-col gap-6;
}
.our-pricing__plans {
  @apply flex flex-col gap-4 min-[900px]:flex-row min-[900px]:max-w-[900px] min-[900px]:mx-auto;
}
</style>
