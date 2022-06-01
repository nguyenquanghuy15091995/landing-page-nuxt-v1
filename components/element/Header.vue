<template>
  <header
    id="header-wrapper"
    class="fixed z-40 top-0 left-0 w-full transition-all duration-300"
  >
    <div
      id="header-contact"
      class="hidden lg:block border-b transition-all duration-300 overflow-hidden"
    >
      <div class="container">
        <div class="flex justify-between items-center py-1">
          <div class="flex items-center gap-2">
            <div class="text-slate-400 text-sm">Find us here:</div>
            <div
              class="text-blue-900 font-semibold cursor-pointer hover:text-rose-500"
            >
              Fb
            </div>
            <div class="h-1.5 w-1.5 border-2 rounded-full border-rose-500" />
            <div
              class="text-blue-900 font-semibold cursor-pointer hover:text-rose-500"
            >
              Ins
            </div>
            <div class="h-1.5 w-1.5 border-2 rounded-full border-rose-500" />
            <div
              class="text-blue-900 font-semibold cursor-pointer hover:text-rose-500"
            >
              In
            </div>
          </div>
          <div class="flex items-center gap-2">
            <div class="text-slate-400 text-sm">Have a question? Call us!</div>
            <div class="text-blue-900 font-semibold cursor-pointer">
              +1 546 987 21 85
            </div>
          </div>
        </div>
      </div>
    </div>
    <div
      id="header-nav"
      class="bg-white shadow lg:shadow-none lg:bg-transparent"
    >
      <div class="container">
        <div class="flex justify-between items-center py-3">
          <div class="z-30 w-full lg:w-auto flex justify-between">
            <img
              src="~assets/icons/ic_logo.svg"
              width="125"
              height="50"
              class="h-8 lg:h-12"
              alt="logo"
            />
            <button class="lg:hidden" @click="toggleMenu()">
              <img
                :src="getUrlImage(isMenuOpen ? 'ic_close' : 'ic_menu')"
                width="30"
                height="30"
                alt="menu"
              />
            </button>
          </div>
          <div
            :class="`fixed z-20 left-0 top-0 w-full h-full lg:w-auto pt-20 lg:pt-0 px-8 lg:px-0 pb-8 lg:pb-0 shadow-md lg:shadow-none lg:relative lg:flex flex-col lg:flex-row lg:items-center gap-10 bg-white lg:bg-transparent ${
              isMenuOpen ? 'flex' : 'hidden'
            }`"
          >
            <ul
              class="flex flex-col lg:flex-row gap-5 lg:gap-10 container px-8 lg:px-0"
            >
              <li>
                <ElementNavLink id="nav-link-service" href="#"
                  >Services</ElementNavLink
                >
              </li>
              <li>
                <ElementNavLink id="nav-link-about" href="#"
                  >About</ElementNavLink
                >
              </li>
              <li>
                <ElementNavLink id="nav-link-step" href="#"
                  >Steps</ElementNavLink
                >
              </li>
              <li>
                <ElementNavLink id="nav-link-price" href="#"
                  >Price</ElementNavLink
                >
              </li>
              <li>
                <ElementNavLink id="nav-link-testimonial" href="#"
                  >Testimonials</ElementNavLink
                >
              </li>
              <li>
                <ElementNavLink id="nav-link-blog" href="#"
                  >Blog</ElementNavLink
                >
              </li>
            </ul>
            <div class="container flex justify-center px-12 lg:p-0">
              <ElementButtonNormal>Get Started</ElementButtonNormal>
            </div>
          </div>
        </div>
      </div>
    </div>
  </header>
</template>

<script lang="ts">
let lastScrollTop = 0;
export default {
  name: "ElementHeader",
  data() {
    return {
      isMenuOpen: false,
    };
  },

  mounted() {
    this.handleScroll();
    window.addEventListener("scroll", this.handleScroll);
  },

  beforeDestroy() {
    window.removeEventListener("scroll", this.handleScroll);
  },

  methods: {
    handleScroll() {
      const headerWrapper = document.getElementById("header-wrapper");
      if (headerWrapper) {
        if (window.scrollY === 0) {
          headerWrapper.classList.remove("lg:bg-white", "lg:shadow");
        } else {
          headerWrapper.classList.add("lg:bg-white", "lg:shadow");
        }
        const st = window.pageYOffset || document.documentElement.scrollTop;
        if (st > lastScrollTop) {
          // downscroll code
          headerWrapper.classList.add("lg:-translate-y-[33px]");
        } else {
          // upscroll code
          headerWrapper.classList.remove("lg:-translate-y-[33px]");
        }
        lastScrollTop = st <= 0 ? 0 : st;
      }
    },
    toggleMenu() {
      this.isMenuOpen = !this.isMenuOpen;
    },
    getUrlImage(iconName) {
      return require(`~/assets/icons/${iconName}.svg`);
    },
  },
};
</script>
