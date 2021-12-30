<template>
  <el-form ref="Form" label-suffix=":" :model="ruleForm">
    <el-form-item label="数字" prop="num" :rules="ruleForm.rules">
      <el-input-number
          v-model="ruleForm.num"
          :controls="false"
      ></el-input-number>
    </el-form-item>
    <el-form-item label="当前输入的数字" prop="num">
      {{ ruleForm.num }}
    </el-form-item>
    <el-form-item>
      <el-button type="primary" @click="submitForm()"> 提交 </el-button>
    </el-form-item>
  </el-form>
  <el-button @click="reset()">reset</el-button>
</template>

<script lang="ts">
import { ref, defineComponent } from 'vue'
export default defineComponent({
  setup() {
    const ruleForm = ref({
      num: undefined,
      rules: [{ required: true, message: '请输入数字' }],
    })
    const Form = ref()
    const submitForm = () => {
      Form.value.validate((valid: any) => {
        if (valid) {
          alert(`submit success with ${ruleForm.value.num}`)
        } else {
          alert(`submit error`)
        }
        return false
      })
    }
    const reset = () => {
      ruleForm.value.num = undefined
    }
    return {
      ruleForm,
      Form,
      submitForm,
      reset,
    }
  },
})
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
