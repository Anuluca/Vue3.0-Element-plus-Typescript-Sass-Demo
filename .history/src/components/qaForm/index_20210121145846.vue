<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs, onMounted } from "vue";

export default defineComponent({
  name: "qaForm",
  setup() {
    // const showForm = {
    //   keyword: "123",
    //     matchType: "precise"
    // }
    const data = reactive({
      showForm: reactive({
        keyword: "123",
        matchType: "precise"
      }),
      jjj:"尼阿美"
    });
    return {
      ...toRefs(data)
    };
  }
});
</script>
<style lang="sass" src="./index.sass"></style>
