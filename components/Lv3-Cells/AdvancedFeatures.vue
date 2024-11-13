<template>
  <div class="advanced-features">
    <AdvancedFeature
      v-for="(feature, index) in advancedFeature"
      :key="index"
      :imageSrc="feature.imageSrc"
      :title="feature.title"
      :description="feature.description"
    />
  </div>
</template>

<script setup lang="ts">
const advancedFeature = [
  {
    imageSrc: "/images/real-time.png",
    title: "Real-Time Property Analytics",
    description:
      "Stay ahead with real-time analytics. Our platform provides comprehensive insights into your property performance, tenant occupancy rates, and market trends. ",
  },
  {
    imageSrc: "/images/security.png",
    title: "Secure Document Storage",
    description:
      "Keep all your important documents in one secure place. Our platform offers encrypted document storage for leases, contracts, and property records.",
  },
  {
    imageSrc: "/images/invoice.png",
    title: "Automated Invoicing",
    description:
      "Simplify your billing process with automated invoicing. Our platform generates and sends invoices to tenants automatically, tracking payments and overdue accounts seamlessly.",
  },
  {
    imageSrc: "/images/reporting.png",
    title: "Customizable Reporting",
    description:
      "Generate detailed, customizable reports with ease. Our reporting tools allow you to create and export reports on occupancy rates, financial performance, maintenance issues, and more",
  },
];
</script>

<style scoped></style>
