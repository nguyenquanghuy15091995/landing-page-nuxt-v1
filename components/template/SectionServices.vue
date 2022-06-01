<template>
  <section class="py-10 lg:py-20">
    <div class="container">
      <div class="row gap-y-5">
        <div
          v-for="(service, serviceIdx) in services"
          :key="`service-${serviceIdx}`"
          class="col-12 md:col-6 lg:col-3"
        >
          <div :class="serviceIdx % 2 !== 0 ? 'md:-translate-y-1/4' : ''">
            <ElementCardService v-bind="service" />
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
import { ImageProps } from "@/utils/images";
export default {
  name: "TemplateSectionServices",
  data() {
    return {
      services: [
        {
          image: new ImageProps(
            "icons/ic_service_seo.svg",
            "service SEO Consultancy"
          ),
          title: "SEO Consultancy",
          description:
            "Dolor enim dolor labore velit nulla sit exercitation proident esse culpa commodo n irure esse velit commodo.",
        },
        {
          image: new ImageProps(
            "icons/ic_service_optimize.svg",
            "service Site Optimization"
          ),
          title: "Site Optimization",
          description:
            "Voluptate in sunt commodo aute do. Dolor enim dolor labore velit nulla sit exetion irure esse proid.",
        },
        {
          image: new ImageProps(
            "icons/ic_service_ranking.svg",
            "service Page Rankings"
          ),
          title: "Page Rankings",
          description:
            "Dolor enim dolor labore velit nulla sit exercitation proident esse culpa commodo n irure esse velit commodo.",
        },
        {
          image: new ImageProps(
            "icons/ic_service_retention.svg",
            "service User Retention"
          ),
          title: "User Retention",
          description:
            "Voluptate in sunt commodo aute do. Dolor enim dolor labore velit nulla sit exetion irure esse proid.",
        },
      ],
    };
  },
};
</script>
