<template src = "./index.html"></template>
<script lang="ts">
import { Component, Emit, Prop, Vue ,Watch } from "vue-property-decorator";
// import ReviewPreview from "@/components/reviewPreview/index.vue";

@Component({
  //注册组件
  components: {
    // "review-preview": ReviewPreview,
  },
})
export default class QaTable extends Vue {

}
</script>
<style lang="scss" src = "./index.scss"></style>