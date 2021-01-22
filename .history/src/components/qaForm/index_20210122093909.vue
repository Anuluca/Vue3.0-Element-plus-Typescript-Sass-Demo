<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs, onMounted } from "vue";

export default defineComponent({
  name: "qaForm",
  setup() {
    // const showForm = reactive({
    //   keyword: "",
    //   matchtype: "precise",
    // });
    const data = reactive({
      showForm:{
        keyword: "",
      matchtype: "precise",
      }

    });


    return {
      // toRef(showForm),
      ...toRefs(data),
    };
  },
});
</script>
<style lang="sass" src="./index.sass"></style>
