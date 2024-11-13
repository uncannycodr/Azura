<template>
  <div class="starter-plan">
    <div class="starter-plan__text">
      <AzuraText tag="p" color="navy" size="2rem" weight="semibold">
        Starter Plan
      </AzuraText>
      <AzuraText tag="p" color="blue-horizon" size="lg" weight="normal">
        For small property owners and managers just getting started.
      </AzuraText>
    </div>

    <!-- ----------- -->
    <div class="starter-plan__plan">
      <div class="starter-plan__price">
        <AzuraText tag="p" color="navy" size="5xl" weight="bold">
          $29.99
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
    <AzuraButton as="button" variant="outline" class="bg-white">
      <AzuraText tag="p" color="navy" size="base" weight="semibold">
        Get Started Now
      </AzuraText>
    </AzuraButton>

    <!-- ----------/ -->
    <div class="starter-plan__features">
      <AzuraText
        tag="p"
        color="navy"
        size="base"
        weight="semibold"
        class="mb-2"
      >
        Starter Plan Features:
      </AzuraText>
      <div class="starter-plan__feature">
        <div class="testimonial-card__image">
          <NuxtImg
            src="/images/check.png"
            alt="logo"
            class="testimonial-card__img h-8 w-8"
          />
        </div>
        <AzuraText tag="p" color="blue-horizon" size="base" weight="normal">
          Manage up to 10 properties
        </AzuraText>
      </div>
      <div class="starter-plan__feature">
        <div class="testimonial-card__image">
          <NuxtImg
            src="/images/check.png"
            alt="logo"
            class="testimonial-card__img h-8 w-8"
          />
        </div>
        <AzuraText tag="p" color="blue-horizon" size="base" weight="normal">
          Basic analytics and reporting
        </AzuraText>
      </div>
      <div class="starter-plan__feature">
        <div class="testimonial-card__image">
          <NuxtImg
            src="/images/check.png"
            alt="logo"
            class="testimonial-card__img h-8 w-8"
          />
        </div>
        <AzuraText tag="p" color="blue-horizon" size="base" weight="normal">
          Secure document storage
        </AzuraText>
      </div>
      <div class="starter-plan__feature">
        <div class="testimonial-card__image">
          <NuxtImg
            src="/images/check.png"
            alt="logo"
            class="testimonial-card__img h-8 w-8"
          />
        </div>
        <AzuraText tag="p" color="blue-horizon" size="base" weight="normal">
          Automated invoicing
        </AzuraText>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.starter-plan {
  @apply bg-chef-hat flex flex-col gap-5 p-8 rounded-xl;
}
.starter-plan__plan {
  @apply flex flex-col gap-2;
}
.starter-plan__price {
  @apply flex flex-row items-end gap-2;
}
.starter-plan__features {
  @apply flex flex-col gap-2;
}

.starter-plan__feature {
  @apply flex flex-row items-center gap-2;
}
</style>
