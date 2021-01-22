<template src="./index.html"></template>
<script lang="ts">
import { Options, Vue } from "vue-class-component";
import QaForm from "@/components/qaForm/index.vue";

@Options({
  components: {
    QaForm,
  },
})
export default class QaTable extends Vue {
  activeName = "first";
}
</script>
<style lang="sass" src="./index.sass"></style>
