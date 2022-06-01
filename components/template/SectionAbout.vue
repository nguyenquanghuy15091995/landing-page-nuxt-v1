<template>
  <section class="py-10 lg:py-20">
    <div class="container">
      <div class="row gap-y-5">
        <div class="col-12 md:col-6 md:order-2">
          <div class="px-6">
            <div class="mb-3">
              <ElementTag>The History</ElementTag>
            </div>
            <div class="mb-6">
              <ElementSectionTitle
                >Our Way To Succesful Future</ElementSectionTitle
              >
            </div>
            <div class="mb-3">
              <ElementSectionSubTitle>
                Sint nulla commodo qui magna eiusmod quis aliqua laboris officia
                excepteur non eu in.
              </ElementSectionSubTitle>
            </div>
            <div class="mb-3">
              <p class="text-slate-500">
                Dolor duis voluptate enim exercitation consequat ex. Voluptate
                in sunt commodo aute do. Dolor enim dolor labore velit nulla sit
                exercitation irure esse proident velit commodo. Est non officia
                proident esse culpa commodo nulla Lorem do enderit esse do.
              </p>
            </div>
            <div>
              <button class="flex gap-3 relative items-stretch group">
                <div
                  class="p-5 relative before:rounded-full before:bg-rose-100 before:absolute before:top-0 before:left-0 before:w-full before:h-full before:duration-300 before:transition-transform before:scale-75 before:group-hover:scale-100"
                >
                  <div
                    class="relative font-semibold text-white w-16 h-16 rounded-full bg-gradient-to-r from-rose-500 via-rose-400 to-rose-300 flex items-center justify-center uppercase"
                  >
                    Play
                  </div>
                </div>
                <div class="flex flex-col items-start justify-center">
                  <div class="text-rose-400 font-semibold uppercase">
                    About Us
                  </div>
                  <div class="text-slate-500">Watch our process!</div>
                </div>
              </button>
            </div>
          </div>
        </div>
        <div class="col-12 md:col-6 md:order-1">
          <div class="flex justify-center">
            <img
              src="~assets/images/img_about.svg"
              width="550"
              height="550"
              alt="about us"
            />
          </div>
        </div>
      </div>
      <div class="row pt-28 pb-10 gap-y-8">
        <div
          v-for="(aboutInfo, infoIdx) in aboutInfos"
          :key="`about-info-${infoIdx}`"
          class="col-12 md:col-6 lg:col-3"
        >
          <ElementAboutItem
            :title="aboutInfo.title"
            :sub-title="aboutInfo.subTitle"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script lang="ts">
export default {
  name: "TemplateSectionAbout",
  data() {
    return {
      aboutInfos: [
        {
          title: "$ 35k",
          subTitle: "CLIENTS REVENUE",
        },
        {
          title: "16k",
          subTitle: "LEADS FOR CLIENTS",
        },
        {
          title: "6.7k",
          subTitle: "PHONE CALLS",
        },
        {
          title: "254",
          subTitle: "SUCCESSFUL PROJECTS",
        },
      ],
    };
  },
};
</script>
