<template src="./index.html"></template>
<script lang="ts">
import { defineComponent, reactive, ref, toRefs, onMounted } from "vue";

export default defineComponent({
  name: "qaForm",
  setup() {
    showForm: ref({
        keyword: "123",
        matchType: "precise"
      })
    const data = reactive({
 
      jjj:"尼阿美"
    });
    return {
      ...toRefs(data)
    };
  }
});
</script>
<style lang="sass" src="./index.sass"></style>
