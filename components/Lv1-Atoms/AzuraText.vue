<script setup lang="ts">
import type { colors } from "~/assets/colors";

type TextColor = keyof typeof colors;
type TextLeading = "sm" | "md" | "lg" | "xl";
type Size =
  | "xs"
  | "sm"
  | "base"
  | "lg"
  | "xl"
  | "1.375rem"
  | "2xl"
  | "2rem"
  | "1.75rem"
  | "3xl"
  | "4xl"
  | "3.625rem"
  | "5xl"
  | "6xl"
  | "62px"
  | "64px"
  | "7xl"
  | "8xl"
  | "9xl";
// 14, 16, 18, 20, 24, 28, 2rem
type FluidSize = "xs" | "sm" | "base" | "lg" | "xl" | "2xl" | "3xl";

interface Props {
  tag:
    | "p"
    | "h1"
    | "h2"
    | "h3"
    | "h4"
    | "h5"
    | "h6"
    | "span"
    | "sup"
    | "sub"
    | "a"
    | "li";
  color?: TextColor;
  leading?: TextLeading; // line height 18, 20, 28, 40
  size?: Size;
  weight?: keyof typeof fontWeightVariants;
  textClass?: HTMLElement["className"] | string;
  fluid?: FluidSize;
}

const props = defineProps<Props>();
const sizeVariants: Record<Size, string> = {
  xs: "text-xs", // 12px
  sm: "text-sm", // 14px
  base: "text-base", // 16px
  lg: "text-lg", // 18px
  xl: "text-xl", // 20px
  "1.375rem": "text-[1.375rem]", // 22px
  "2xl": "text-2xl", // 24px
  "1.75rem": "text-[1.75rem]", // 28px
  "3xl": "text-3xl", // 30px
  "2rem": "text-[2rem]", // 32px
  "4xl": "text-4xl", // 36px
  "5xl": "text-5xl", // 48px
  "3.625rem": "text-[3.625rem]", // 56px
  "6xl": "text-6xl", // 60px
  "62px": "text-[62px]", // 62px
  "64px": "text-[64px]", // 64px
  "7xl": "text-7xl", // 72px
  "8xl": "text-8xl", // 96px
  "9xl": "text-9xl", // 128px
};
const fluidVariants: Record<FluidSize, string> = {
  xs: "font-xs", // 16px - 18px
  sm: "font-sm", // 16px - 28px
  base: "font-base", // 18px - 28px
  lg: "font-lg", // 18px - 58px
  xl: "font-xl", // 36px - 48px
  "2xl": "font-2xl", // 48px - 64px
  "3xl": "font-3xl", // 48px - 72px
};
const colorVariants: Record<TextColor, string> = {
  aria: "text-aria",
  navy: "text-navy",
  white: "text-white",
  "faded-denim": "text-faded-denim",
  "chef-hat": "text-chef-hat",
  "blue-horizon": "text-blue-horizon",
  "dodger-blue": "text-dodger-blue",
  orochimaru: "text-orochimaru",
  sambucus: "text-sambucus",
};

const leadVariants: Record<TextLeading, string> = {
  sm: "leading-[1.125rem]",
  md: "leading-5",
  lg: "leading-7",
  xl: "leading-10",
};

const fontWeightVariants: Record<string, string> = {
  thin: "font-thin", // 100
  extralight: "font-extralight", // 200
  light: "font-light", // 300
  normal: "font-normal", // 400
  medium: "font-medium", // 500
  semibold: "font-semibold", // 600
  bold: "font-bold", // 700
  extrabold: "font-extrabold", // 800
  black: "font-black", // 900
};

const classes = computed(() => [
  sizeVariants[props.size as Size],
  fluidVariants[props.fluid as FluidSize],
  colorVariants[props.color as TextColor],
  props.leading ? leadVariants[props.leading as TextLeading] : "",
  props.weight ? fontWeightVariants[props.weight] : "",
]);

// console.log(classes);
</script>

<template>
  <component :is="tag" :class="classes">
    <slot />
  </component>
</template>

<style scoped></style>
