<template>
  <div class="footer">
    <div class="footer__top">
      <div class="footer__top-left">
        <div class="footer__image">
          <NuxtImg
            src="/images/logo.png"
            alt="logo"
            class="footer__img w-34 h-12"
          />
        </div>
        <AzuraText tag="p" color="blue-horizon" size="xl" weight="normal">
          Empowering Property Owners with Cutting-Edge Management Tools
        </AzuraText>
        <div class="footer__links">
          <IconBrandLinkedin class="w-[28px] h-[28px] text-blue-horizon" />
          <IconBrandInstagram class="w-[29px] h-[29px] text-blue-horizon" />
          <IconBrandTwitterFilled class="w-[28px] h-[28px] text-blue-horizon" />
        </div>
      </div>
      <div class="footer__top-right">
        <FooterForm />
      </div>
    </div>

    <div class="footer__bottom">
      <AzuraText
        tag="p"
        color="blue-horizon"
        size="base"
        weight="semibold"
        class="border-b border-blue-horizon hover:cursor-pointer hover:opacity-[0.7] hover:border-opacity-[0.7] max-w-[249px]"
      >
        Designed by Breeje Anadkat
      </AzuraText>
      <AzuraText tag="p" color="blue-horizon" size="base" weight="light">
        © 2024 Azura. All rights reserved.
      </AzuraText>
      <div class="flex flex-row gap-8">
        <AzuraText
          tag="p"
          color="blue-horizon"
          size="base"
          weight="semibold"
          class="border-b border-blue-horizon hover:cursor-pointer hover:opacity-[0.7] hover:border-opacity-[0.7]"
        >
          Built in Framer
        </AzuraText>
        <AzuraText
          tag="p"
          color="blue-horizon"
          size="base"
          weight="semibold"
          class="border-b border-blue-horizon hover:cursor-pointer hover:opacity-[0.7] hover:border-opacity-[0.7]"
        >
          Get This Template
        </AzuraText>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import {
  IconBrandInstagram,
  IconBrandLinkedin,
  IconBrandTwitterFilled,
} from "@tabler/icons-vue";
</script>

<style scoped>
.footer {
  @apply max-w-[1312px] mx-auto px-6 flex flex-col gap-10 py-24;
}
.footer__top {
  @apply flex flex-row justify-between max-[1000px]:flex-col gap-8;
}
.footer__top-left {
  @apply max-w-[530px] flex flex-col gap-8;
}
.footer__links {
  @apply flex flex-row gap-4 cursor-pointer;
}
.footer__bottom {
  @apply border-t border-gray-400 flex max-[1000px]:flex-col gap-2  flex-row justify-between pt-8;
}
</style>
