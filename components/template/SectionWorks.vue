<template>
  <section class="pb-10 lg:pb-0">
    <div class="container relative">
      <div class="hidden lg:flex justify-between absolute top-3 left-0 w-full">
        <img
          src="~assets/images/img_leaf_01.svg"
          width="70"
          height="70"
          alt="left leaf"
        />
        <img
          src="~assets/images/img_leaf_02.svg"
          width="70"
          height="70"
          alt="right leaf"
        />
      </div>
      <div class="relative">
        <div class="flex justify-center mb-3">
          <ElementTag>WHAT WE DO</ElementTag>
        </div>
        <div class="text-center mb-5">
          <ElementSectionTitle>What You Will Get With Us</ElementSectionTitle>
        </div>
        <div class="text-center">
          <ElementSectionSubTitle>
            Dolor duis voluptate enim exercitation consequat ex.
          </ElementSectionSubTitle>
        </div>
        <div class="row gap-y-5 lg:translate-y-10">
          <div
            v-for="(work, workIdx) in works"
            :key="`work-${workIdx}`"
            class="col-12 md:col-6 lg:col-4"
          >
            <div :class="isTranslateDown(workIdx) ? 'lg:translate-y-10' : ''">
              <ElementCardWork v-bind="work" />
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { ImageProps } from "@/utils/images";
export default {
  name: "TemplateSectionWorks",
  data() {
    return {
      works: [
        {
          icon: new ImageProps(
            "icons/ic_work_research_analysis.svg",
            "Research & Analysis"
          ),
          title: "Research & Analysis",
          description:
            "Dolor duis voluptate enim exercitation consequat ex. Voluptate in sunt commodo aute do. Dolor enim dolor labore velit nulla sit exercitation irure esse proid.",
        },
        {
          icon: new ImageProps(
            "icons/ic_work_unique_content.svg",
            "Unique Content"
          ),
          title: "Unique Content",
          description:
            "Voluptate in sim dolor labore velit nuunt commodo aute do. Dolor enim dolor labore im dolor labore velit te dolor enim dolor labore velit nul.",
        },
        {
          icon: new ImageProps(
            "icons/ic_work_thematic_link.svg",
            "Thematic Links"
          ),
          title: "Thematic Links",
          description:
            "Pariatur magna cupidatat magna sit incididunt non pariatur. Sint nulla commodo qui magna eiusmod quis aliqua laboris officia excepteur non eu in.",
        },
        {
          icon: new ImageProps(
            "icons/ic_work_effective_design.svg",
            "Effective UX/UI Design"
          ),
          title: "Effective UX/UI Design",
          description:
            "Pariatur magna cupidatat magna sit incididunt non pariatur. Sint nulla commodo qui magna eiusmod quis aliqua laboris officia excepteur non eu in.",
        },
        {
          icon: new ImageProps(
            "icons/ic_work_responsive_speed.svg",
            "Responsive & High Speed"
          ),
          title: "Responsive & High Speed",
          description:
            "Dolor duis voluptate enim exercitation consequat ex. Voluptate in sunt commodo aute do. Dolor enim dolor labore velit nulla sit exercitation irure esse proid.",
        },
        {
          icon: new ImageProps(
            "icons/ic_work_quality_valid.svg",
            "Quality & Valid Code"
          ),
          title: "Quality & Valid Code",
          description:
            "Voluptate in sim dolor labore velit nuunt commodo aute do. Dolor enim dolor labore im dolor labore velit te dolor enim dolor labore velit nul.",
        },
      ],
    };
  },
  methods: {
    isTranslateDown(itemIdx) {
      if (Array.isArray(this.works)) {
        const maxCol = 3;
        let counter = 0;
        const maxRow = Math.ceil(this.works.length / 3);
        for (let i = 0; i < maxRow; i++) {
          for (let j = 0; j < maxCol; j++) {
            if (counter === itemIdx && j === 1) {
              return true;
            }
            counter++;
          }
        }
      }
      return false;
    },
  },
};
</script>
