<template>
  <div class="home">
    <AzuraHeader />
    <HeroSection />
    <AzuraAbout />
    <FeaturesSection />
    <TestimonialSection />
    <OurPricing />
    <FAQ />
    <CTA />
    <AzuraFooter />

    <!-- <AzuraText tag="p" color="dodger-blue" size="4xl" weight="bold">
      Today is a Good Day!
    </AzuraText> -->
    <!-- <AzuraButton as="button" variant="primary">
      <AzuraText tag="p" color="white" size="base" weight="semibold">
        Contact Us
      </AzuraText>
    </AzuraButton>
    <AzuraButton as="button" variant="outline">
      <AzuraText tag="p" color="navy" size="base" weight="semibold">
        Learn More
      </AzuraText>
    </AzuraButton> -->
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.home {
  @apply relative overflow-hidden;
}
</style>
