<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";
import QaForm from "@/components/qaForm/index.vue";
import { questionData,answerData } from "./mock";

export default defineComponent({
  name: "qaModel",
  components: {
    QaForm,
  },
  setup() {
    const data = reactive({
      activeName: "first",
      questionData: questionData,
      answerData: answerData,

      handleSelectionChange: () => {
        data.activeName="second"
      },
      backToQuestion:() => {
        data.activeName="first"
      }
    });

    return {
      ...toRefs(data),
    };
  },
});
</script>
<style lang="sass" src="./index.sass"></style>
