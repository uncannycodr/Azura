<template>
  <div class="pro-plan">
    <div class="pro-plan__text">
      <AzuraText tag="p" color="navy" size="2rem" weight="semibold">
        Pro Plan
      </AzuraText>
      <AzuraText tag="p" color="blue-horizon" size="lg" weight="normal">
        For property owners and managers seeking advanced features.
      </AzuraText>
    </div>

    <!-- ----------- -->
    <div class="pro-plan__plan">
      <div class="pro-plan__price">
        <AzuraText tag="p" color="navy" size="5xl" weight="bold">
          $79.99
        </AzuraText>
        <AzuraText tag="p" color="blue-horizon" size="base" weight="normal">
          /m
        </AzuraText>
      </div>
      <AzuraText tag="p" color="blue-horizon" size="sm" weight="normal">
        Pause or cancel anytime
      </AzuraText>
    </div>

    <!-- --------- -->
    <AzuraButton as="button" variant="primary">
      <AzuraText tag="p" color="white" size="base" weight="semibold">
        Get Started Now
      </AzuraText>
    </AzuraButton>

    <!-- ----------/ -->
    <div class="pro-plan__features">
      <AzuraText
        tag="p"
        color="navy"
        size="base"
        weight="semibold"
        class="mb-2"
      >
        Everything in Starter Plan, plus:
      </AzuraText>
      <div class="pro-plan__feature">
        <div class="pro-plan__image">
          <NuxtImg
            src="/images/check2.png"
            alt="logo"
            class="pro-plan__img h-8 w-8"
          />
        </div>
        <AzuraText tag="p" color="blue-horizon" size="base" weight="normal">
          Manage unlimited properties
        </AzuraText>
      </div>
      <div class="pro-plan__feature">
        <div class="pro-plan__image">
          <NuxtImg
            src="/images/check2.png"
            alt="logo"
            class="pro-plan__img h-8 w-8"
          />
        </div>
        <AzuraText tag="p" color="blue-horizon" size="base" weight="normal">
          Advanced analytics and reporting
        </AzuraText>
      </div>
      <div class="pro-plan__feature">
        <div class="pro-plan__image">
          <NuxtImg
            src="/images/check2.png"
            alt="logo"
            class="pro-plan__img h-8 w-8"
          />
        </div>
        <AzuraText tag="p" color="blue-horizon" size="base" weight="normal">
          Integrated payment processing
        </AzuraText>
      </div>
      <div class="pro-plan__feature">
        <div class="pro-plan__image">
          <NuxtImg
            src="/images/check2.png"
            alt="logo"
            class="pro-plan__img h-8 w-8"
          />
        </div>
        <AzuraText tag="p" color="blue-horizon" size="base" weight="normal">
          Everything on starter plan plus
        </AzuraText>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.pro-plan {
  @apply bg-anakiwa flex flex-col gap-5 p-8 border-dodger-blue border-4 rounded-xl;
}
.pro-plan__plan {
  @apply flex flex-col gap-2;
}
.pro-plan__price {
  @apply flex flex-row items-end gap-2;
}
.pro-plan__features {
  @apply flex flex-col gap-2;
}

.pro-plan__feature {
  @apply flex flex-row items-center gap-2;
}
</style>
