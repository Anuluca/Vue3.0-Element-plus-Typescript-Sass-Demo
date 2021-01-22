<template src="./index.html"></template>
<script lang="ts">
import { Options, Vue } from "vue-class-component";

@Options({

})
export default class QaForm extends Vue {
    showForm={
        keyword:'123',
        matchType:'precise'
    }

}
</script>
<style lang="sass" src="./index.sass"></style>
