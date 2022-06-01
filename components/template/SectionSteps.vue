<template>
  <section class="py-10 lg:py-20">
    <div class="container relative">
      <div class="hidden lg:flex justify-between absolute top-3 left-0 w-full">
        <img
          src="~assets/images/img_leaf_01.svg"
          width="70"
          height="70"
          alt="left leaf"
        />
      </div>
      <div class="relative">
        <div class="flex justify-center mb-3">
          <ElementTag>STEPS</ElementTag>
        </div>
        <div class="text-center mb-16">
          <ElementSectionTitle>Main Milestones</ElementSectionTitle>
        </div>
        <div class="row gap-y-3 mb-10">
          <div
            v-for="(step, stepIdx) in steps"
            :key="`step-${stepIdx}`"
            class="col-6 lg:col-3"
          >
            <ElementCardStep
              v-bind="step"
              :counter-number="
                stepIdx + 1 < 10 ? `0${stepIdx + 1}` : `${stepIdx + 1}`
              "
            />
          </div>
        </div>
        <div class="flex justify-center">
          <p
            class="uppercase text-center text-slate-500 text-sm font-semibold max-w-3xl"
          >
            PARIATUR MAGNA CUPIDATAT MAGNA SIT INCIDIDUNT NON PARIATUR. SINT
            NULLA COMMODO QUI MAGNA EIUSMOD QUIS ALIQUA LABORIS OFFICIA
            EXCEPTEUR NON EU IN. CONSEQUAT ESSE IN DOLORE LABORUM DOLORE UT DUIS
            ELIT DESERUNT MINIM.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { ImageProps } from "@/utils/images";
export default {
  name: "TemplateSectionSteps",
  data() {
    return {
      steps: [
        {
          icon: new ImageProps("icons/ic_step_planning.svg", "Planning"),
          title: "Planning",
        },
        {
          icon: new ImageProps("icons/ic_step_research.svg", "Research"),
          title: "Research",
        },
        {
          icon: new ImageProps(
            "icons/ic_step_optimization.svg",
            "Optimization"
          ),
          title: "Optimization",
        },
        {
          icon: new ImageProps("icons/ic_step_results.svg", "Results"),
          title: "Results",
        },
      ],
    };
  },
};
</script>
