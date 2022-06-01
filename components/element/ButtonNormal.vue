<template>
  <button
    v-bind="$props"
    class="text-white bg-blue-900 rounded-full w-full px-7 py-2 font-semibold text-md transition-colors shadow-md hover:bg-rose-400 active:bg-rose-500"
  >
    <slot />
  </button>
</template>

<script lang="ts">
export default {
  name: "ElementButtonNormal",
};
</script>
