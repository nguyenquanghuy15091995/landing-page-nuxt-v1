<template>
  <div
    class="relative w-full h-full max-h-[13rem] max-w-[13rem] rounded-2xl bg-white shadow-rocket flex justify-center items-center p-5"
  >
    <a :href="href" class="absolute left-0 top-0 w-full h-full"></a>
    <img
      :src="getUrlImage(image.src)"
      width="100"
      height="100"
      class="object-contain w-full max-w-[80%] max-h-[80%]"
      :alt="image.alt"
    />
  </div>
</template>

<script lang="ts">
import { ImageProps } from "@/utils/images";
export default {
  name: "ElementCardLogo",
  props: {
    image: {
      type: ImageProps,
      required: true,
    },
    href: {
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
