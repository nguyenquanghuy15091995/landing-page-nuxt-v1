<template>
  <section class="py-10 lg:py-0">
    <div class="container">
      <div class="row justify-center lg:-translate-y-1/3">
        <div
          v-for="(logo, logoIdx) in logos"
          :key="`logo-${logoIdx}`"
          :class="`w-1/2 md:w-[30%] lg:w-1/5 p-3 flex justify-center items-center${
            logoIdx % 2 === 0 ? '' : ' lg:-translate-y-10'
          }`"
        >
          <ElementCardLogo v-bind="logo" />
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { ImageProps } from "@/utils/images";
export default {
  name: "TemplateSectionLogos",
  data() {
    return {
      logos: [
        {
          image: new ImageProps("images/img_logo_01.svg", "Logo 1"),
          href: "#",
        },
        {
          image: new ImageProps("images/img_logo_02.svg", "Logo 2"),
          href: "#",
        },
        {
          image: new ImageProps("images/img_logo_03.svg", "Logo 3"),
          href: "#",
        },
        {
          image: new ImageProps("images/img_logo_04.svg", "Logo 4"),
          href: "#",
        },
        {
          image: new ImageProps("images/img_logo_05.svg", "Logo 5"),
          href: "#",
        },
      ],
    };
  },
};
</script>
