<template>
  <a
    :id="id"
    :href="href"
    class="relative py-1.5 pl-4 lg:pl-0 text-slate-400 transition-colors hover:text-rose-500 before:scale-0 before:transition-transform before:p-0.5 before:border-2 before:rounded-full before:border-rose-500 before:absolute before:top-1/2 before:lg:top-0 before:left-0 before:lg:left-1/2 before:-translate-y-1/4 before:lg:translate-y-0 before:lg:-translate-x-1/2"
  >
    <slot />
  </a>
</template>

<script lang="ts">
export default {
  name: "ElementNavLink",
  props: {
    href: {
      type: String,
      default: "#",
    },
    id: {
      type: String,
      required: true,
    },
  },
};
</script>
