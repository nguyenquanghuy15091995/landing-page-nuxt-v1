<template>
  <section class="py-10 lg:py-20">
    <div class="container relative pb-10 lg:pb-0">
      <div class="hidden lg:flex justify-end absolute top-8 left-0 w-full">
        <img
          src="~assets/images/img_leaf_02.svg"
          width="70"
          height="70"
          alt="right leaf"
        />
      </div>
      <div class="relative">
        <div class="flex justify-center mb-3">
          <ElementTag>Prices</ElementTag>
        </div>
        <div class="text-center mb-6">
          <ElementSectionTitle>Discover Our Price - List</ElementSectionTitle>
        </div>
        <div class="text-center mb-11">
          <ElementSectionSubTitle
            >Dolor duis voluptate enim exercitation consequat
            ex.</ElementSectionSubTitle
          >
        </div>
        <div class="row items-stretch justify-center lg:items-center gap-y-5">
          <div
            v-for="(price, priceIdx) in prices"
            :key="`price-${priceIdx}`"
            class="col-12 md:col-6 lg:col-4"
          >
            <ElementCardPrice v-bind="price" />
          </div>
        </div>
      </div>
    </div>
    <div class="bg-[#eaeef9] py-10 lg:pb-20 lg:pt-40 lg:-mt-32">
      <div class="container">
        <div class="row gap-y-5">
          <div class="col-12 lg:col-5 lg:order-2 flex justify-center">
            <img
              src="~assets/images/img_newsletter.svg"
              width="483"
              height="381"
              alt="newsletter"
            />
          </div>
          <div class="col-12 lg:col-7 lg:order-1 flex flex-col justify-center">
            <div class="mb-4 text-blue-900 font-semibold text-3xl lg:text-4xl">
              Newsletter
            </div>
            <p class="mb-3 text-slate-500">
              Pariatur magna cupidatat magna sit incididunt non pariatur. Sint
              nulla commodo qui magna eiusmod quis aliqua laboris officia
              excepteur non eu in.
            </p>
            <form class="flex flex-col lg:flex-row gap-3">
              <input
                type="email"
                class="min-h-[3.75rem] rounded-full shadow-rocket px-6 ring-0 outline-none w-full"
                placeholder="Enter your email"
              />
              <ElementButtonGradient type="button"
                >Subscribe</ElementButtonGradient
              >
            </form>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: "TemplateSectionPrices",
  data() {
    return {
      prices: [
        {
          category: "Simple",
          title: "Basic Plan",
          cost: 69.95,
          services: [
            "Monthly Progress Report",
            "Ad Campaign Management",
            "Business Page Optimization",
            "Copywriter & Visual Design",
          ],
        },
        {
          category: "MEDIUM",
          title: "Standard Plan",
          cost: 89.95,
          services: [
            "Basic Plan",
            "Ad Campaign Management",
            "Business Page Optimization",
            "Copywriter & Visual Design",
            "Monthly Progress Report",
            "Social Media Listening",
          ],
          isRecommended: true,
        },
        {
          category: "extended",
          title: "Power Plan",
          cost: 99.95,
          services: [
            "Monthly Progress Report",
            "Ad Campaign Management",
            "Business Page Optimization",
            "Copywriter & Visual Design",
          ],
        },
      ],
    };
  },
};
</script>
