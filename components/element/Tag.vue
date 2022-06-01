<template>
  <div
    class="relative uppercase pl-5 text-rose-500 font-medium before:p-0.5 before:absolute before:border-2 before:border-rose-500 before:rounded-full before:left-0 before:top-1/2 before:-translate-y-1/3"
  >
    <slot />
  </div>
</template>

<script lang="ts">
export default {
  name: "ElementTag",
};
</script>
