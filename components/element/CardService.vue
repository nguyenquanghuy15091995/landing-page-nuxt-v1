<template>
  <div
    class="relative shadow-rocket rounded-2xl pt-12 pb-10 px-6 bg-white overflow-hidden before:absolute before:top-3 before:left-1/2 before:-translate-y-1/2 before:-translate-x-1/2 before:p-14 before:rounded-full before:border-[3rem] before:border-slate-100"
  >
    <div class="relative">
      <div class="flex justify-center mb-8">
        <img
          :src="getUrlImage(image.src)"
          width="70"
          height="70"
          :alt="image.alt"
        />
      </div>
      <div class="text-blue-900 font-bold text-center text-xl mb-2">
        {{ title }}
      </div>
      <div class="text-center text-slate-500">{{ description }}</div>
    </div>
  </div>
</template>

<script lang="ts">
import { ImageProps } from "@/utils/images";
export default {
  name: "ElementCardService",
  props: {
    image: {
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
