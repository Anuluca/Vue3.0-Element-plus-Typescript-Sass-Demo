<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";
import QaForm from "@/components/qaForm/index.vue";
import { questionData } from "./mock";

export default defineComponent({
  name: "qaModel",
  components: {
    QaForm,
  },
  setup() {
    const data = reactive({
      activeName: "first",
      questionData: questionData,

      handleSelectionChange: () => {
        activeName:"second"
        alert(1);
      },
    });

    return {
      ...toRefs(data),
    };
  },
});
</script>
<style lang="sass" src="./index.sass"></style>
