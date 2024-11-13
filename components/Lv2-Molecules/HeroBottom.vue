<template>
  <div class="hero-bottom">
    <AzuraText
      tag="p"
      color="navy"
      size="xl"
      weight="normal"
      class="leading-[30px] text-center"
    >
      TRUSTED BY LEADING REAL ESTATE COMPANIES WORLDWIDE
    </AzuraText>
    <div class="hero-bottom__logos-wrapper">
      <div class="hero-bottom__logos">
        <!-- Duplicate logos to create seamless looping -->
        <div class="hero-bottom__logo" v-for="i in 5" :key="i">
          <NuxtImg
            :src="'/images/logo' + i + '.png'"
            alt="logo"
            class="hero-bottom__img max-w-[200px]"
          />
        </div>
        <!-- Repeat the same set of logos for seamless loop -->
        <div class="hero-bottom__logo" v-for="i in 5" :key="'repeat-1-' + i">
          <NuxtImg
            :src="'/images/logo' + i + '.png'"
            alt="logo"
            class="hero-bottom__img max-w-[200px]"
          />
        </div>
        <!-- Another set for more seamless loop -->
        <div class="hero-bottom__logo" v-for="i in 5" :key="'repeat-2-' + i">
          <NuxtImg
            :src="'/images/logo' + i + '.png'"
            alt="logo"
            class="hero-bottom__img"
          />
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.hero-bottom {
  @apply flex flex-col items-center gap-12;
}

.hero-bottom__logos-wrapper {
  @apply relative w-full overflow-hidden; /* Fixed width and hiding overflow */
  max-width: 1200px;
  height: 100px;
  mask-image: linear-gradient(
    to right,
    transparent 0%,
    black 15%,
    black 85%,
    transparent 100%
  );
}

.hero-bottom__logos {
  @apply flex items-center;
  display: flex;
  gap: 4rem;
  animation: infinite-scroll 20s linear infinite; /* Increased duration for smoother loop */
  width: calc(15 * 100px); /* Adjusted width for three sets of 5 logos */
}

.hero-bottom__logo {
  @apply flex-shrink-0;
}

@keyframes infinite-scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(
      -100%
    ); /* Move left by the full width of the entire logo set */
  }
}
</style>
