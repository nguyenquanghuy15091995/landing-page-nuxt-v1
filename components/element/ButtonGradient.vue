<template>
  <button
    v-bind="$props"
    class="group relative text-white bg-rose-500 rounded-full min-h-[3.75rem] px-10 flex items-center justify-center text-lg font-semibold shadow-lg overflow-hidden active:shadow"
  >
    <div
      class="absolute left-0 right-0 w-full h-full rounded-full bg-gradient-to-r from-transparent via-red-300 to-transparent duration-300 transition-transform scale-150 translate-x-1/3 group-hover:-translate-x-1/3 group-active:-translate-x-1/2"
    />
    <span class="relative">
      <slot />
    </span>
  </button>
</template>

<script lang="ts">
export default {
  name: "ElementButtonGradient",
};
</script>
