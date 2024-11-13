<template>
  <div class="cta">
    <!-- Desktop (Visible above 800px) -->
    <div class="cta__desktop hidden md:flex">
      <div class="cta__content">
        <AzuraText
          tag="p"
          color="navy"
          size="5xl"
          weight="semibold"
          class="leading-[64px]"
        >
          Transform Your Property Management Today!
        </AzuraText>
        <div>
          <AzuraButton as="button" variant="secondary">
            <AzuraText tag="p" color="navy" size="base" weight="semibold">
              Get Started Now
            </AzuraText>
          </AzuraButton>
        </div>
      </div>
    </div>

    <!-- Mobile (Visible below 800px) -->
    <div class="cta__mobile flex md:hidden">
      <div class="cta__content">
        <AzuraText
          tag="p"
          color="navy"
          size="5xl"
          weight="semibold"
          class="leading-[64px]"
        >
          Transform Your Property Management Today!
        </AzuraText>

        <AzuraButton as="button" variant="secondary">
          <AzuraText tag="p" color="navy" size="base" weight="semibold">
            Get Started Now
          </AzuraText>
        </AzuraButton>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.cta {
  @apply bg-black py-28 px-4;
}

.cta__desktop {
  @apply max-w-[1280px] mx-auto rounded-xl bg-slate-600 h-[480px] items-center justify-center relative;
  background: url("/images/mansion1.png") bottom left no-repeat,
    url("/images/mansion2.png") bottom right no-repeat,
    radial-gradient(circle, rgb(87, 182, 255) 58%, rgb(182, 216, 255) 100%);
  background-size: 300px auto, 300px auto, cover; /* Adjust sizes as needed */
}

.cta__mobile {
  @apply max-w-[1280px] mx-auto rounded-xl bg-slate-600 h-[480px] items-center justify-center relative px-4;
  background: radial-gradient(
    circle,
    rgb(87, 182, 255) 58%,
    rgb(182, 216, 255) 100%
  );
}

.cta__content {
  @apply max-w-[800px] flex flex-col justify-center gap-6 text-center;
}

.cta__button {
  @apply bg-white text-black font-semibold py-2 px-4 rounded-lg transition-all;
}
.cta__button:hover {
  @apply bg-gray-200;
}
</style>
