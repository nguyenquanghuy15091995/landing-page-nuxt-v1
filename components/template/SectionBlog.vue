<template>
  <section class="py-10 lg:py-20">
    <div class="container">
      <div class="flex justify-center mb-3">
        <ElementTag>NEWS</ElementTag>
      </div>
      <div class="text-center mb-6">
        <ElementSectionTitle>Read Our Blog</ElementSectionTitle>
      </div>
      <div class="text-center mb-7">
        <ElementSectionSubTitle
          >Dolor duis voluptate enim exercitation consequat
          ex.</ElementSectionSubTitle
        >
      </div>
      <div class="flex justify-center mb-11">
        <ElementButtonGradient>View All</ElementButtonGradient>
      </div>
      <div class="row gap-y-5">
        <div
          v-for="(blog, blogIdx) in blogs"
          :key="`blog-${blogIdx}`"
          class="col-12 md:col-6"
        >
          <ElementCardBlog v-bind="blog" />
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { ImageProps } from "@/utils/images";
export default {
  name: "TemplateSectionBlog",
  data() {
    return {
      blogs: [
        {
          image: new ImageProps("images/img_news_01.jpg", "news 01"),
          title:
            "Dolor duis voluptate enim exercitation consequat ex. Voluptate in sunt",
          date: "Jun 25, 2021",
          author: "Annette Black",
        },
        {
          image: new ImageProps("images/img_news_02.jpg", "news 02"),
          title:
            "Dolor duis voluptate enim exercitation consequat ex. Voluptate in sunt",
          date: "Jun 25, 2021",
          author: "Dianne Russell",
        },
      ],
    };
  },
};
</script>
