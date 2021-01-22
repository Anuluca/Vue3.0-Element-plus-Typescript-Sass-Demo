<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs, onMounted } from "vue";

export default defineComponent({
  name: "qaForm",
  setup() {
    const showForm = reactive({
      keyword: "2132",
      matchtype: "precise",
    });
    const data = reactive({
      
    });


    return {
      showForm,
      ...toRefs(data),
    };
  },
});
</script>
<style lang="sass" src="./index.sass"></style>
