<template>
  <div class="faq">
    <div class="faq__text">
      <AzuraText tag="p" color="navy" size="5xl" weight="semibold">
        Frequently Asked Questions
      </AzuraText>
      <AzuraText tag="p" color="blue-horizon" size="xl" weight="normal">
        Find answers to common questions about our platform and services.
      </AzuraText>

      <div>
        <AzuraButton as="button" variant="primary">
          <AzuraText tag="p" color="white" size="base" weight="semibold">
            Contact Us
          </AzuraText>
        </AzuraButton>
      </div>
    </div>
    <Accordion
      :items="accordionItemsWithoutIcons"
      width="80%"
      variant="chevron"
      class="pt-0"
    />
  </div>
</template>

<script setup lang="ts">
const accordionItemsWithoutIcons = [
  {
    title: "What is Azura and how can it help me?",
    content:
      "Our free trial gives you full access to all features of the Pro Plan for 14 days. You can explore and test the platform without any commitment. At the end of the trial, you can choose a plan that best suits your needs.",
  },
  {
    title: "How does the free trial work?",
    content:
      "Our free trial gives you full access to all features of the Pro Plan for 14 days. You can explore and test the platform without any commitment. At the end of the trial, you can choose a plan that best suits your needs.",
  },
  {
    title: "Can I upgrade or downgrade my plan at any time?",
    content:
      "Our free trial gives you full access to all features of the Pro Plan for 14 days. You can explore and test the platform without any commitment. At the end of the trial, you can choose a plan that best suits your needs.",
  },
  {
    title: "How secure is my data with Azura?",
    content:
      "Our free trial gives you full access to all features of the Pro Plan for 14 days. You can explore and test the platform without any commitment. At the end of the trial, you can choose a plan that best suits your needs.",
  },
  {
    title: "What kind of support is available to me?",
    content:
      "Our free trial gives you full access to all features of the Pro Plan for 14 days. You can explore and test the platform without any commitment. At the end of the trial, you can choose a plan that best suits your needs.",
  },
];
</script>

<style scoped>
.faq {
  @apply max-w-[1312px] px-4 mx-auto flex lg:flex-row flex-col gap-8 items-center lg:justify-between py-24;
}
.faq__text {
  @apply flex flex-col gap-4;
}
</style>
