<template>
  <div class="features">
    <div class="features__text">
      <AzuraText
        tag="p"
        color="navy"
        size="5xl"
        weight="semibold"
        class="leading-[64px]"
      >
        Discover Azura's Powerful Real Estate Tools
      </AzuraText>
      <AzuraText tag="p" color="navy" size="xl" weight="normal">
        Explore advanced features designed to streamline property management and
        optimize your investments.
      </AzuraText>
    </div>
    <!-- -------desktop-------- -->
    <div class="flex flex-row justify-between max-[1280px]:hidden">
      <div class="wrapper">
        <FeatureImages />
      </div>
      <AdvancedFeatures class="w-1/2" />
    </div>

    <!-- ---------mobile--------- -->

    <div class="mobile flex flex-col gap-8 min-[1280px]:hidden">
      <!-- ------1-- -->
      <div class="flex flex-col gap-8">
        <div class="content flex flex-col gap-4">
          <div class="icon">
            <NuxtImg src="/images/invoice.png" alt="logo" />
          </div>
          <AzuraText tag="p" color="navy" size="2rem" weight="semibold">
            Real-Time Property Analytics
          </AzuraText>
          <AzuraText tag="p" color="blue-horizon" size="xl" weight="normal">
            Stay ahead with real-time analytics. Our platform provides
            comprehensive insights into your property performance, tenant
            occupancy rates, and market trends.
          </AzuraText>
        </div>

        <div
          class="image-wrapper bg-chef-hat flex flex-col items-center px-4 pt-8 rounded-xl"
        >
          <div class="image">
            <NuxtImg src="/images/image1.png" alt="logo" class="img w-64" />
          </div>
        </div>
      </div>

      <!-- ----------2 -->
      <div class="flex flex-col gap-8">
        <div class="content flex flex-col gap-4">
          <div class="icon">
            <NuxtImg src="/images/invoice.png" alt="logo" />
          </div>
          <AzuraText tag="p" color="navy" size="2rem" weight="semibold">
            Real-Time Property Analytics
          </AzuraText>
          <AzuraText tag="p" color="blue-horizon" size="xl" weight="normal">
            Stay ahead with real-time analytics. Our platform provides
            comprehensive insights into your property performance, tenant
            occupancy rates, and market trends.
          </AzuraText>
        </div>

        <div
          class="image-wrapper bg-chef-hat flex flex-col items-center px-4 pt-8 rounded-xl"
        >
          <div class="image">
            <NuxtImg src="/images/image1.png" alt="logo" class="img w-64" />
          </div>
        </div>
      </div>

      <!-- -------------3 -->

      <div class="flex flex-col gap-8">
        <div class="content flex flex-col gap-4">
          <div class="icon">
            <NuxtImg src="/images/invoice.png" alt="logo" />
          </div>
          <AzuraText tag="p" color="navy" size="2rem" weight="semibold">
            Real-Time Property Analytics
          </AzuraText>
          <AzuraText tag="p" color="blue-horizon" size="xl" weight="normal">
            Stay ahead with real-time analytics. Our platform provides
            comprehensive insights into your property performance, tenant
            occupancy rates, and market trends.
          </AzuraText>
        </div>

        <div
          class="image-wrapper bg-chef-hat flex flex-col items-center px-4 pt-8 rounded-xl"
        >
          <div class="image">
            <NuxtImg src="/images/image1.png" alt="logo" class="img w-64" />
          </div>
        </div>
      </div>

      <!-- ----------4 -->

      <div class="flex flex-col gap-8">
        <div class="content flex flex-col gap-4">
          <div class="icon">
            <NuxtImg src="/images/invoice.png" alt="logo" />
          </div>
          <AzuraText tag="p" color="navy" size="2rem" weight="semibold">
            Real-Time Property Analytics
          </AzuraText>
          <AzuraText tag="p" color="blue-horizon" size="xl" weight="normal">
            Stay ahead with real-time analytics. Our platform provides
            comprehensive insights into your property performance, tenant
            occupancy rates, and market trends.
          </AzuraText>
        </div>

        <div
          class="image-wrapper bg-chef-hat flex flex-col items-center px-4 pt-8 rounded-xl"
        >
          <div class="image">
            <NuxtImg src="/images/image1.png" alt="logo" class="img w-64" />
          </div>
        </div>
      </div>
    </div>
  </div>

  <!-- mobile -->
</template>

<script setup lang="ts"></script>

<style scoped>
.features {
  @apply max-w-[1312px] mx-auto px-6 py-28 flex flex-col gap-20;
}
.features__text {
  @apply max-w-[700px] mx-auto items-center text-center flex flex-col gap-6;
}
</style>
