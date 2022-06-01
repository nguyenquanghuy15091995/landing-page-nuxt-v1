<template>
  <section class="py-10 lg:py-20 gap-y-5">
    <div class="container">
      <div class="row gap-y-5">
        <div class="col-12 lg:col-7 flex justify-center lg:justify-start">
          <img
            src="~assets/images/img_testimonials.svg"
            width="583"
            height="529"
            alt="Testimonials"
          />
        </div>
        <div class="col-12 lg:col-5 flex flex-col justify-center">
          <div class="mb-3">
            <ElementTag>THEY SAY</ElementTag>
          </div>
          <div class="mb-6">
            <ElementSectionTitle>Testimonials</ElementSectionTitle>
          </div>
          <p class="text-slate-500 mb-5">
            “Dolor duis voluptate enim exercitation consequat ex. Voluptate in
            sunt commodo aute do. Dolor enim dolor labore velit nulla sit
            exercitation irure esse proident.”
          </p>
          <div class="flex gap-3">
            <div class="rounded-full bg-slate-100 w-16 h-16"></div>
            <div class="flex flex-col justify-center gap-1">
              <div class="text-blue-900 uppercase font-semibold text-sm">
                Ahihi Ahihi
              </div>
              <div class="text-slate-500 text-sm">Marketing Something</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: "TemplateSectionTestimonials",
};
</script>
