<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png" />
    <HelloWorld msg="Elementui+ Demo" />
    <el-button type="primary" @click="addLibQa">进入问答{{qaDrawer}}</el-button>
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
import { defineComponent, reactive, ref, toRefs } from "vue";
import HelloWorld from "@/components/HelloWorld.vue"; // @ is an alias to /src
import QaModel from "@/components/qaModel/index.vue";

export default defineComponent({
  name: "Home",
  components: {
    HelloWorld,
    QaModel
  },
  setup() {
    const data = reactive({
      qaDrawer: true,
      isQa: true,
      selectQaMode: "",
      selectModule: 0,

      addLibQa: () => {
        setTimeout(() => {
          data.qaDrawer = true;
          data.isQa = true;
          data.selectQaMode = "qaMode";
          data.selectModule = 0;
          // setTimeout(() => {
          //   (this.$refs["qaChild"] as QaModel).getFatherData();
          // }, 0);
        }, 0);
      }
    });
    return {
      ...toRefs(data)
    };
  }
});
</script>
