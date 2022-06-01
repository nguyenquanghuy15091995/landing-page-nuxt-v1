<template>
  <div v-if="variant === 'h1'" class="rocket-heading-1">
    <h1 class="text-blue-900 font-bold text-4xl md:text-6xl lg:text-7xl">
      <slot />
    </h1>
  </div>
  <div v-else class="rocket-heading-2">
    <h2 class="text-blue-900 font-bold text-3xl md:text-4xl lg:text-5xl">
      <slot />
    </h2>
  </div>
</template>

<script lang="ts">
export default {
  name: "ElementSectionTitle",
  props: {
    variant: {
      type: String,
      default: "h2",
    },
  },
};
</script>
