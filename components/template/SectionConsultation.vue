<template>
  <section class="py-10 lg:pt-40 lg:pb-0 bg-[#eaeef9] overflow-hidden">
    <div class="container relative">
      <div class="row items-end">
        <div class="col-12 lg:col-5 flex flex-col justify-center lg:pb-40">
          <div class="mb-3">
            <ElementTag>GET STARTED</ElementTag>
          </div>
          <div class="mb-6">
            <ElementSectionTitle>Get A Free Consultation</ElementSectionTitle>
          </div>
          <div class="mb-9">
            <p class="text-slate-500 text-sm">
              Dolor duis voluptate enim exercitation consequat ex. Voluptate in
              sunt commodo aute dolor enim dolor labore velit nul.
            </p>
          </div>
          <form>
            <div class="row gap-y-5">
              <div class="col-12 md:col-6">
                <input
                  type="text"
                  class="min-h-[3.75rem] rounded-full shadow-rocket px-6 ring-0 outline-none w-full"
                  placeholder="First name"
                />
              </div>
              <div class="col-12 md:col-6">
                <input
                  type="text"
                  class="min-h-[3.75rem] rounded-full shadow-rocket px-6 ring-0 outline-none w-full"
                  placeholder="Last name"
                />
              </div>
              <div class="col-12 md:col-6">
                <input
                  type="text"
                  class="min-h-[3.75rem] rounded-full shadow-rocket px-6 ring-0 outline-none w-full"
                  placeholder="Enter your phone"
                />
              </div>
              <div class="col-12 md:col-6">
                <input
                  type="email"
                  class="min-h-[3.75rem] rounded-full shadow-rocket px-6 ring-0 outline-none w-full"
                  placeholder="Enter your Email"
                />
              </div>
              <div
                class="col-12 md:col-4 lg:col-5 xl:col-4 flex justify-center md:justify-start"
              >
                <ElementButtonGradient type="button"
                  >Submit</ElementButtonGradient
                >
              </div>
              <div
                class="col-12 md:col-8 lg:col-7 xl:col-8 flex items-center justify-center md:justify-start"
              >
                <input
                  id="acceptCheck"
                  type="checkbox"
                  class="cursor-pointer"
                />
                <div
                  class="cursor-pointer pl-2 mb-0.5 font-semibold text-slate-500"
                >
                  <label for="acceptCheck" class="cursor-pointer"
                    >I accept the</label
                  >
                  <a href="#" class="text-rose-400 hover:text-rose-500"
                    >Terms and Conditions.</a
                  >
                </div>
              </div>
            </div>
          </form>
        </div>
        <div class="hidden lg:block col-7">
          <img
            src="~assets/images/img_consultation.svg"
            width="776"
            height="791"
            class="-mb-5"
            alt="consultation"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: "TemplateSectionConsultation",
};
</script>
