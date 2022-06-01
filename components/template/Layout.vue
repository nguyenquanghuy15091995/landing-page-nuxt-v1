<template>
  <div>
    <ElementHeader />
    <main>
      <slot />
    </main>
    <footer class="py-6 border-t">
      <div class="container">
        <div class="flex justify-between items-center">
          <img
            src="~assets/icons/ic_logo.svg"
            width="75"
            height="25"
            alt="logo"
          />
          <div class="text-slate-500 text-sm">
            ©All rights reserved. Huy Ed. Nguyen 2022
          </div>
        </div>
      </div>
    </footer>
  </div>
</template>

<script lang="ts">
export default {
  name: "TemplateLayout",
};
</script>
