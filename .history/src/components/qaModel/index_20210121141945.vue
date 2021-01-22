<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";
import QaForm from "@/components/qaForm/index.vue";

export default defineComponent({
  name: "qaModel",
  components: {
    QaForm
  },
  setup() {
    const data = reactive({
      activeName: "first",
    });
    return {
      ...toRefs(data)
    };
  }
});
</script>
<style lang="sass" src="./index.sass"></style>
