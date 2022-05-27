<template>
  <q-page padding>
    <q-select
      v-model="locale"
      :options="localeOptions"
      label="Quasar Language"
      dense
      borderless
      emit-value
      map-options
      options-dense
      style="max-width: 150px"
    />

    <div>
      {{ "key1: " + $t("key1") }}
    </div>
    <div>
      {{ "key2: " + $t("key2") }}
    </div>
    <div>
      key3:
      <span v-html="content"></span>
    </div>
  </q-page>
</template>

<script>
import { ref, watch } from "vue";
import { useI18n } from "vue-i18n";

export default {
  data() {
    return {
      content: this.$t("key3"),
    };
  },

  setup() {
    const { locale } = useI18n({ useScope: "global" });

    return {
      locale,
      localeOptions: [
        { value: "en-US", label: "English" },
        { value: "de", label: "German" },
      ],
    };
  },
};
</script>
