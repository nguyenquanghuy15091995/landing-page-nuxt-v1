<template>
  <div
    class="overflow-hidden h-full rounded-2xl shadow-rocket bg-white group cursor-pointer"
  >
    <div class="overflow-hidden">
      <img
        :src="getUrlImage(image.src)"
        width="555"
        height="310"
        class="object-cover w-full transition-transform duration-500 group-hover:scale-125"
        :alt="image.alt"
      />
    </div>
    <div class="px-6 lg:px-10 xl:px-7 pb-10">
      <div
        class="py-4 flex flex-wrap gap-3 items-center border-b text-sm md:text-base"
      >
        <div class="text-slate-500">{{ date }}</div>
        <div class="p-0.5 border border-rose-500 rounded-full" />
        <div class="text-slate-500 text-sm md:text-base">{{ author }}</div>
      </div>
      <div class="pt-4">
        <div class="text-blue-900 text-lg md:text-xl lg:text-2xl font-semibold">
          {{ title }}
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import { ImageProps } from "@/utils/images";
export default {
  name: "ElementCardBlog",
  props: {
    image: {
      type: ImageProps,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    date: {
      type: String,
      required: true,
    },
    author: {
      type: String,
      required: true,
    },
    href: {
      type: String,
      default: "#",
    },
  },
  methods: {
    getUrlImage(src) {
      return require(`~/assets/${src}`);
    },
  },
};
</script>
