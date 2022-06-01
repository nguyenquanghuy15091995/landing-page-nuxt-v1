<template>
  <div
    class="relative flex flex-col items-center justify-center min-h-[10rem] before:absolute before:left-1/2 before:top-1/2 before:-translate-x-1/2 before:-translate-y-1/2 before:border-[2.5rem] before:border-slate-100 before:p-10 before:rounded-full"
  >
    <div
      class="relative font-semibold text-5xl text-blue-900 mb-3 flex items-center justify-center gap-2"
    >
      <span>{{ title }}</span>
      <span class="text-rose-400 text-3xl">+</span>
    </div>
    <div class="relative uppercase font-medium text-slate-500">
      {{ subTitle }}
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "ElementAboutItem",
  props: {
    title: {
      type: String,
      required: true,
    },
    subTitle: {
      type: String,
      required: true,
    },
  },
};
</script>
