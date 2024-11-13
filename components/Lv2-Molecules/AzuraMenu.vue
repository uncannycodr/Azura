<template>
  <ul class="menu">
    <DynaText
      v-for="(item, index) in headerLinks"
      :key="index"
      tag="li"
      color="black"
      size="base"
      weight="medium"
    >
      <NuxtLink :to="item.link">{{ item.text }}</NuxtLink>
    </DynaText>
  </ul>
</template>

<script setup lang="ts">
const headerLinks = [
  { text: "Features", link: "/" },
  { text: "Testimonials", link: "/" },
  { text: "Pricing", link: "/" },
  { text: "FAQs", link: "/" },
];
</script>

<style scoped>
.menu {
  @apply lg:flex flex-row gap-6 hidden;
}
</style>
