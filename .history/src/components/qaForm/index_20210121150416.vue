<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs, onMounted } from "vue";

export default defineComponent({
  name: "qaForm",
  setup() {
    const showForm = reactive({
      keyword: "",
      matchType: "precise",
    });
    const data = reactive({
      jjj: "尼阿美",
    });
    return {
      showForm,
      ...toRefs(data),
    };
  },
});
</script>
<style lang="sass" src="./index.sass"></style>
