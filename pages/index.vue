<template>
  <TemplateLayout>
    <div id="service" class="topic-wrapper">
      <TemplateSectionHero />
      <TemplateSectionServices />
    </div>
    <div id="about" class="topic-wrapper">
      <TemplateSectionAbout />
      <TemplateSectionWorks />
      <TemplateSectionConsultation />
      <TemplateSectionLogos />
    </div>
    <div id="step" class="topic-wrapper">
      <TemplateSectionSteps />
    </div>
    <div id="price" class="topic-wrapper">
      <TemplateSectionPrices />
    </div>
    <div id="testimonial" class="topic-wrapper">
      <TemplateSectionTestimonials />
    </div>
    <div id="blog" class="topic-wrapper">
      <TemplateSectionBlog />
    </div>
  </TemplateLayout>
</template>

<script lang="ts">
import Vue from "vue";
export default Vue.extend({
  name: "IndexPage",
  mounted() {
    this.handleCheckActive();
    window.addEventListener("scroll", this.handleCheckActive);
  },

  beforeDestroy() {
    window.removeEventListener("scroll", this.handleCheckActive);
  },

  methods: {
    handleCheckActive() {
      const topicWrappers = document.getElementsByClassName("topic-wrapper");
      let activeId = null;
      for (let i = 0; i < topicWrappers.length; i++) {
        const boundary = topicWrappers[i].getBoundingClientRect();
        if (boundary.top < window.screen.height / 3) {
          activeId = topicWrappers[i].id;
        }
      }
      for (let i = 0; i < topicWrappers.length; i++) {
        if (topicWrappers[i].id !== activeId) {
          const navLink = document.getElementById(
            `nav-link-${topicWrappers[i].id}`
          );
          if (navLink) {
            navLink.classList.add("text-slate-400", "before:scale-0");
            navLink.classList.remove("text-rose-500", "before:scale-100");
          }
        }
      }
      if (activeId) {
        const navLink = document.getElementById(`nav-link-${activeId}`);
        if (navLink) {
          navLink.classList.add("text-rose-500", "before:scale-100");
          navLink.classList.remove("text-slate-400", "before:scale-0");
        }
      }
    },
  },
});
</script>
