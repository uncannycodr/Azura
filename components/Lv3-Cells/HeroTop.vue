<template>
  <div class="hero-top">
    <div class="hero-top__content">
      <div class="hero-top__text">
        <AzuraText
          tag="p"
          color="navy"
          size="3.625rem"
          weight="semibold"
          class="leading-[74px]"
        >
          Optimize and Grow Your Real Estate Portfolio with Azura
        </AzuraText>
        <AzuraText tag="p" color="blue-horizon" size="xl" weight="normal">
          Experience seamless property management and take control of your
          portfolio effortlessly.
        </AzuraText>
      </div>
      <div class="hero-top__btn">
        <AzuraButton as="button" variant="primary">
          <AzuraText tag="p" color="white" size="base" weight="semibold">
            Get Started Now
          </AzuraText>
        </AzuraButton>
        <AzuraButton as="button" variant="outline">
          <AzuraText tag="p" color="navy" size="base" weight="semibold">
            Learn More
          </AzuraText>
        </AzuraButton>
      </div>
    </div>
    <div class="hero-top__image">
      <NuxtImg src="/images/hero.png" alt="logo" class="hero-top__img" />
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.hero-top {
  @apply flex lg:flex-row flex-col pl-6  justify-between items-center relative w-full object-cover overflow-visible gap-12;
}

.hero-top__content {
  @apply flex flex-col gap-16 lg:max-w-[708px]  flex-shrink-0;
}

.hero-top__text {
  @apply flex flex-col gap-8;
}

.hero-top__btn {
  @apply flex md:flex-row gap-4 flex-col pr-2;
}

.hero-top__image {
  @apply lg:max-w-[1000px] lg:left-[20px] w-full relative  flex-shrink-0 overflow-hidden object-cover;
}

.hero-top__img {
  @apply w-full h-full relative overflow-hidden object-cover  flex-shrink-0 rounded-xl;
}
</style>
