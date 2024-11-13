<template>
  <div :style="{ width: width }" class="p-4">
    <div class="space-y-4">
      <!-- Add spacing between each FAQ item -->
      <div
        v-for="(item, index) in items"
        :key="index"
        class="group rounded-lg shadow-md p-4 bg-chef-hat"
      >
        <div :class="headerClasses" @click="toggleAccordion(index)">
          <!-- Start Icon -->
          <div class="mr-4">
            <component
              :is="isOpen(index) ? iconMinus : iconPlus"
              class="h-6 w-6 text-primary transition-all duration-300"
            />
          </div>

          <!-- Title -->
          <AzuraText tag="h1" color="navy" size="lg" class="flex-1">
            {{ item.title }}
          </AzuraText>
        </div>

        <!-- Expandable Content with Transition -->
        <transition name="accordion">
          <AzuraText
            tag="p"
            color="navy"
            size="base"
            class="p-4 bg-gray-50 rounded-b-lg"
            v-if="isOpen(index)"
          >
            {{ item.content }}
          </AzuraText>
        </transition>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { IconMinus, IconPlus } from "@tabler/icons-vue";
import { computed, defineProps, ref } from "vue";

interface Props {
  items: Array<{ title: string; content: string; icon?: any }>;
  variant?: "icon" | "chevron" | "simple";
  width?: string;
}

const props = defineProps<Props>();

const openIndex = ref(-1);
const isOpen = (index: number) => openIndex.value === index;
const toggleAccordion = (index: number) => {
  openIndex.value = isOpen(index) ? -1 : index;
};

const headerClasses = computed(() => [
  "flex items-start cursor-pointer justify-start  text-lg font-medium text-navy bg-pink",
]);

const iconPlus = IconPlus;
const iconMinus = IconMinus;
</script>

<style scoped>
.accordion-enter-active,
.accordion-leave-active {
  transition: max-height 0.3s ease;
}
.accordion-enter-from,
.accordion-leave-to {
  max-height: 0;
  overflow: hidden;
}
.accordion-enter-to,
.accordion-leave-from {
  max-height: 1000px;
  overflow: hidden;
}

/* Background and Divider Colors */
.bg-lightGray {
  background-color: var(--chef-hat);
}
.divide-darkGray {
  border-color: #0f3b68;
}
</style>
