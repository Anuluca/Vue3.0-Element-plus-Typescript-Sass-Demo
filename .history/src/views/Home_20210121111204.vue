<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js + TypeScript App" />
    <el-button type="primary" @click="addLibQa">进入问答</el-button>
    <el-drawer
      v-model="qaDrawer"
      :withHeader="false"
      size="1100px"
      class="search-drawer"
      append-to-body
    >
      <QaModel :isQa="isQa" :selectQaMode="selectQaMode" ref="qaChild">
      </QaModel>
    </el-drawer>
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src
import QaModel from "@/components/qaModel/index.vue";

@Options({
  components: {
    HelloWorld,
    QaModel,
  },
})
export default class Home extends Vue {
  qaDrawer = false;
  isQa = true;
  selectQaMode = '';
  selectModule = 0;

  addLibQa() {
    setTimeout(() => {
      this.qaDrawer = true;
      this.isQa = true;
      this.selectQaMode = 'qaMode';
      this.selectModule = 0;
      // setTimeout(() => {
      //   (this.$refs["qaChild"] as QaModel).getFatherData();
      // }, 0);
    }, 0);
  }

  return{
    
  }
}
</script>
