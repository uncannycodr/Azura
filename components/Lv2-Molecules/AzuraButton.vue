<template>
  <component :is="as" :class="btnClasses">
    <component :is="leftIcon" class="w-4 h-4 text-white font-bold" />
    <span>
      <slot />
    </span>
    <component :is="rightIcon" class="w-5 h-5 ml-2" />
  </component>
</template>

<script setup lang="ts">
interface Props {
  leftIcon?: object;
  rightIcon?: object;
  as: string | object;
  variant?: "primary" | "secondary" | "outline" | "header";
}

const props = defineProps<Props>();

const btnClasses = computed(() => [
  "btn",
  props.variant ? `btn--${props.variant}` : "", // Modifier for variant
]);
</script>

<style scoped>
.btn {
  @apply inline-flex items-center justify-center;
}

.btn--primary {
  @apply text-sm font-semibold leading-5 py-[12px] px-[24px]  rounded-full gap-[6px]  bg-dodger-blue text-white cursor-pointer hover:opacity-90 hover:shadow-md;
}
.btn--secondary {
  @apply text-sm font-semibold leading-5 py-[12px] px-[24px]  rounded-full gap-[6px]  bg-white  cursor-pointer hover:opacity-90 hover:shadow-md;
}
.btn--outline {
  @apply text-sm font-semibold leading-5 py-[12px] px-[24px]  rounded-full flex items-center justify-center gap-[6px]  outline outline-1 outline-aria text-white cursor-pointer hover:shadow-md;
}
</style>
