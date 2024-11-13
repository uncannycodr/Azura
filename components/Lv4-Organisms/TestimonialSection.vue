<template>
  <div class="testimonial">
    <div class="wrapper">
      <div class="testimonial__text">
        <AzuraText
          tag="p"
          color="navy"
          size="5xl"
          weight="semibold"
          class="leading-[64px]"
        >
          What Our Happy Clients Are Saying
        </AzuraText>
        <AzuraText tag="p" color="navy" size="xl" weight="normal">
          Hear from satisfied clients who have transformed their property
          management experience with our platform.
        </AzuraText>
      </div>
      <div class="flex flex-col gap-6">
        <div class="cards">
          <Testimonialcard
            v-for="card in testimonialCards"
            :key="card.name"
            :imageSrc="card.imageSrc"
            :description="card.description"
            :photoSrc="card.photoSrc"
            :name="card.name"
            :position="card.position"
          />
        </div>
        <div class="cards">
          <Testimonialcard
            v-for="card in testimonialCards"
            :key="card.name"
            :imageSrc="card.imageSrc"
            :description="card.description"
            :photoSrc="card.photoSrc"
            :name="card.name"
            :position="card.position"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
const testimonialCards = [
  {
    imageSrc: "/images/coma.png",
    description:
      "The tenant management tools are fantastic. Communication is seamless, and keeping track of leases and payments has never been easier. Highly recommend Azura!",
    photoSrc: "/images/person.png",
    name: "John Doe",
    position: "CEO",
  },
  {
    imageSrc: "/images/coma.png",
    description:
      "The tenant management tools are fantastic. Communication is seamless, and keeping track of leases and payments has never been easier. Highly recommend Azura!",
    photoSrc: "/images/person.png",
    name: "John Doe",
    position: "CEO",
  },
  {
    imageSrc: "/images/coma.png",
    description:
      "The tenant management tools are fantastic. Communication is seamless, and keeping track of leases and payments has never been easier. Highly recommend Azura!",
    photoSrc: "/images/person.png",
    name: "John Doe",
    position: "CEO",
  },
];
</script>

<style scoped>
.testimonial {
  @apply bg-chef-hat py-28 px-6;
}
.wrapper {
  @apply flex flex-col gap-20 items-center;
}
.testimonial__text {
  @apply max-w-[615px] items-center text-center flex flex-col gap-6;
}
.cards {
  @apply flex flex-col gap-6 lg:flex-row;
}
</style>
