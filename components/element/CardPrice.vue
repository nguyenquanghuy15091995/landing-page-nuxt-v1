<template>
  <div
    class="rounded-2xl cursor-pointer bg-white shadow-rocket group h-full lg:h-auto overflow-hidden"
  >
    <div class="relative">
      <div class="py-11 px-9 relative overflow-hidden">
        <div
          class="rounded-full w-full scale-110 origin-bottom h-96 absolute bottom-0 left-1/2 -translate-x-1/2 bg-slate-50"
        />
        <div
          class="rounded-full w-full origin-bottom h-96 absolute bottom-0 left-1/2 -translate-x-1/2 bg-gradient-to-tl from-blue-100 via-white to-white transition-transform duration-300 scale-x-0 group-hover:scale-110"
        />
        <div class="relative">
          <div
            class="uppercase text-rose-500 font-semibold text-center mb-2 text-sm"
          >
            {{ category }}
          </div>
          <div class="text-blue-900 text-xl font-semibold text-center mb-3">
            {{ title }}
          </div>
          <div class="flex items-start justify-center pl-3 mb-1">
            <span class="text-slate-500 text-lg font-semibold pt-2">$</span>
            <span
              class="mx-1 text-blue-900 text-6xl font-bold transition-colors duration-300 group-hover:text-rose-500"
              >{{ filteredCost[0] }}</span
            >
            <span class="text-slate-500 text-lg font-semibold pt-2"
              >.{{ filteredCost[1] }}</span
            >
          </div>
          <div class="text-center text-slate-500">/Per Month</div>
        </div>
      </div>
      <div class="pt-9 pb-11 px-9 relative overflow-hidden">
        <ul class="mb-9">
          <li
            v-for="(service, serviceIdx) in services"
            :key="`price-service-${serviceIdx}`"
            class="text-center text-slate-500 text-sm mb-2"
          >
            {{ service }}
          </li>
        </ul>
        <div class="flex justify-center">
          <button
            class="shadow-rocket bg-blue-900 bg-opacity-10 rounded-full h-10 px-7 font-semibold text-blue-900 transition-colors duration-300 group-hover:bg-opacity-100 group-hover:text-white"
          >
            Buy Now
          </button>
        </div>
        <div
          v-if="isRecommended"
          class="flex justify-center items-center gap-2 mt-7"
        >
          <input type="checkbox" checked />
          <div class="mb-0.5 text-slate-500">Recommended</div>
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  name: "ElementCardPrice",
  props: {
    category: {
      type: String,
      required: true,
    },
    title: {
      type: String,
      required: true,
    },
    cost: {
      type: Number,
      required: true,
    },
    services: {
      type: Array,
      required: true,
    },
    isRecommended: {
      type: Boolean,
      default: false,
    },
  },
  computed: {
    filteredCost() {
      return [
        Math.floor(this.cost),
        ((this.cost - Math.floor(this.cost)) * 100).toFixed(0),
      ];
    },
  },
};
</script>
