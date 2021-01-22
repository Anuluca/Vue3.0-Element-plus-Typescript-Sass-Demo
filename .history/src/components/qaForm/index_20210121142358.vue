<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs, onMounted } from "vue";

export default defineComponent({
  name: "qaForm",
  setup() {
    const data = reactive({
      showForm: {
        keyword: "123",
        matchType: "precise"
      },
    });
    return {
      ...toRefs(data)
    };
  }
});
</script>
<style lang="sass" src="./index.sass"></style>
