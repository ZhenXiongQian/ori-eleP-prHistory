<template>
  <div style="margin-top: 10px">
    <el-button @click="setDisabledFalse">设置disabled为false</el-button>
  </div>
  <div style="margin-top: 10px">
    <el-tooltip ref="tooltipRef2" :disabled="isDisabled" placement="bottom">
      <template #content> multiple lines<br />second line </template>
      <el-button>
        <span @click="setDisabled"> 点击会设置disabled </span>
      </el-button>
    </el-tooltip>
  </div>
  <div style="margin-top: 10px">
    <el-tooltip placement="bottom">
      <template #content> multiple lines<br />second line </template>
      <el-button>原始版本</el-button>
    </el-tooltip>
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
const isDisabled = ref(false)
function setDisabled() {
  isDisabled.value = true
}
function setDisabledFalse() {
  isDisabled.value = false
}
</script>
