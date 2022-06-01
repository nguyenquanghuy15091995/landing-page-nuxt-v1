<template>
  <div class="relative">
    <div
      class="absolute left-0 bottom-0 w-full text-center text-9xl text-slate-300 font-bold text-opacity-50 tracking-wide"
    >
      {{ counterNumber }}
    </div>
    <div class="relative py-8 flex flex-col justify-center items-center gap-5">
      <div>
        <img
          :src="getUrlImage(icon.src)"
          width="70"
          height="70"
          class="min-h-[4.375rem] max-h-[4.375rem]"
          :alt="icon.alt"
        />
      </div>
      <div class="text-blue-900 text-xl font-semibold">{{ title }}</div>
    </div>
  </div>
</template>

<script lang="ts">
import { ImageProps } from "@/utils/images";
export default {
  name: "ElementCardStep",
  props: {
    icon: {
      type: ImageProps,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    counterNumber: {
      type: [String, Number],
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
