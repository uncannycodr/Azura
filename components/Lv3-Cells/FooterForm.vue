<template>
  <div class="form">
    <AzuraText tag="p" color="navy" size="lg" weight="semibold">
      Subscribe to our newsletter
    </AzuraText>
    <div class="form__input-wrapper">
      <input type="email" placeholder="name@email.com" class="form__input" />
      <div class="flex-shrink-0">
        <AzuraButton as="button" variant="primary">
          <AzuraText tag="p" color="white" size="base" weight="semibold">
            Subscribe
          </AzuraText>
        </AzuraButton>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts"></script>

<style scoped>
.form {
  @apply flex flex-col gap-2;
}
.form__input-wrapper {
  @apply flex flex-row items-center gap-2;
}
.form__input {
  @apply w-full rounded-3xl  bg-chef-hat   py-[10px] px-5 text-gray-700 placeholder-gray-400 focus:border-none focus:outline-none focus:ring-dodger-blue sm:text-sm;
}
</style>
