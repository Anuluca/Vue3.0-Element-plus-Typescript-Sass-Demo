<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs, onMounted, toRef } from "vue";

export default defineComponent({
  name: "qaForm",
  setup() {
    const showForm = toRefs({
      keyword: "",
      matchtype: "precise",
    });
    const data = reactive({

    });
    // const showForm2 = toRefs(showForm)

    return {
      showForm,
      ...toRefs(data),
    };
  },
});
</script>
<style lang="sass" src="./index.sass"></style>
