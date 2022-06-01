<template>
  <section
    class="relative pt-14 pb-10 lg:pt-28 lg:pb-20 bg-gradient-to-b from-[#f7f9fc] to-transparent"
  >
    <img
      src="~assets/images/img_bg_hero.svg"
      width="1920"
      height="1208"
      class="object-fill object-top absolute left-0 bottom-0 w-full h-full opacity-40 lg:opacity-100"
      alt="hero banner"
    />
    <div class="relative container pt-10 pb-20">
      <div class="row">
        <div class="col-12 lg:col-6">
          <div class="mb-3">
            <ElementTag>Be Sure</ElementTag>
          </div>
          <div class="mb-4">
            <ElementSectionTitle variant="h1"
              >Your Success Is In Our Hands</ElementSectionTitle
            >
          </div>
          <div class="mb-14">
            <ElementSectionSubTitle
              >Agency with 12 years of history, 15 employees, Fortune 5000
              clients and proven results.</ElementSectionSubTitle
            >
          </div>
          <div>
            <ElementButtonGradient>Learn more</ElementButtonGradient>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: "TemplateSectionHero",
};
</script>
