<template>
  <el-form v-model="formModel">
    <el-form-item label="是否禁用" prop="Status1">
      <el-switch
        v-model="formModel.Status1"
        active-text="启用汉"
        className="isc-switch"
        inactive-text="禁用汉"
        inline-prompt
        width="60"
      />
    </el-form-item>
    <el-form-item label="是否禁用" prop="Status2">
      <el-switch
        v-model="formModel.Status2"
        active-text="on"
        className="isc-switch"
        inactive-text="off"
        inline-prompt
        width="60"
      />
    </el-form-item>
  </el-form>
</template>

<script setup lang="ts">
import { reactive } from "vue";

const formModel = reactive({
  Status1: "",
  Status2: "",
});
</script>

<style lang="scss">
html,
body {
  width: 100vw;
  height: 100vh;
  margin: 0;

  #play {
    height: 100%;
    width: 100%;

    .play-container {
      height: 100%;
      width: 100%;
      display: flex;
      align-items: center;
      justify-content: center;
    }
  }
}
</style>
