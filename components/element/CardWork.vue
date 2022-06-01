<template>
  <div
    class="relative h-full rounded-2xl bg-white shadow-rocket py-8 px-6 overflow-hidden before:absolute before:top-5 before:left-5 before:-translate-y-1/2 before:-translate-x-1/2 before:p-12 before:rounded-full before:border-[2.75rem] before:border-slate-100"
  >
    <div class="relative">
      <div class="flex gap-2 items-center mb-4">
        <img
          :src="getUrlImage(icon.src)"
          width="50"
          height="50"
          :alt="icon.alt"
        />
        <div class="font-semibold text-xl text-blue-900 truncate">
          {{ title }}
        </div>
      </div>
      <p class="text-slate-500 text-sm">{{ description }}</p>
    </div>
  </div>
</template>

<script lang="ts">
import { ImageProps } from "@/utils/images";
export default {
  name: "ElementCardService",
  props: {
    icon: {
      type: ImageProps,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    description: {
      type: String,
      required: true,
    },
  },
  methods: {
    getUrlImage(src) {
      return require(`~/assets/${src}`);
    },
  },
};
</script>
