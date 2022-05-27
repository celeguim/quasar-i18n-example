<template>
  <q-page class="flex flex-center">
    <img
      alt="Quasar logo"
      src="~assets/quasar-logo-vertical.svg"
      style="width: 200px; height: 200px"
    />
  </q-page>
</template>

<script>
import { defineComponent } from "vue";
// import i18n from "boot/i18n";
import { i18n } from "boot/i18n";

console.log(i18n.global.t("success"));
console.log(i18n);

export default defineComponent({
  name: "IndexPage",
});
</script>
