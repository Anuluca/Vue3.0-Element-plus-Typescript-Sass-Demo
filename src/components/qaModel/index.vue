<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs } from "vue";
import QaForm from "@/components/qaForm/index.vue";
import { questionData, answerData } from "./mock";

export default defineComponent({
  name: "qaModel",
  components: {
    QaForm,
  },
  setup() {
    const answerTable = ref(null);
    const data = reactive({
      activeName: "first",
      questionData: questionData,
      answerData: answerData,
      ifClickedRow: -1,

      selectQuestion: (selection: any, row: any) => {
        console.log("我在这里", selection, row);
        data.activeName = "second";
      },
      selectQuestionRow: (column: any) => {
        console.log("当前点击的是整行");
        data.selectQuestion([], column);
      },
      backToQuestion: () => {
        data.activeName = "first";
      },
      jumpToAnswer: (index: any) => {
        data.ifClickedRow = index;
        setTimeout(() => {
          (answerTable.value as any).scrollTop = 512 * index;
        }, 0);
      },
    });

    return {
      answerTable,
      ...toRefs(data),
    };
  },
});
</script>
<style lang="sass" src="./index.sass"></style>
