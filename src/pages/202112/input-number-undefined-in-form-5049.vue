<template>
  <el-form ref="ruleForm" label-suffix=":" :model="form">
    <el-form-item
      label="数字"
      prop="num"
      :rules="[{ required: true, message: '请输入数字' }]"
    >
      <el-input-number
        v-model="form.num"
        placeholder="please input number"
      ></el-input-number>
    </el-form-item>
    <el-form-item label="当前输入的数字" prop="num">
      {{ form.num }}
    </el-form-item>
    <el-form-item>
      <el-button type="primary" @click="submitForm()"> 提交 </el-button>
    </el-form-item>
  </el-form>
  <el-button @click="setNull"> setNull </el-button>
  <el-button @click="setUndefined"> setUndefined </el-button>
</template>

<script setup lang="ts">
import { ref } from "vue";
const ruleForm = ref();
const form = ref({
  num: undefined,
});
function submitForm() {
  ruleForm.value.validate((valid: any) => {
    if (valid) {
      alert(`submit success with: ${form.value.num}`);
    } else {
      alert(`submit failed`);
    }
  });
}
function setNull() {
  form.value.num = null;
}
function setUndefined() {
  form.value.num = undefined;
}
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
