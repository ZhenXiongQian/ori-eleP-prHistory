<template>
  <div>
    <h2>5106</h2>
    <el-select-v2
        v-model="value1"
        :options="options"
        placeholder="Please select"
        size="large"
    ></el-select-v2>
    <el-button @click="clear1">清空</el-button>
    <el-button @click="set1">设置</el-button>
    <p>{{ value1 }}</p>
  </div>
  <el-divider></el-divider>
  <div>
    <h2>5107</h2>
    <el-select-v2
        v-model="value2"
        :options="options"
        :multiple="true"
        placeholder="Please select"
        style="width: 200px"
        size="large"
    ></el-select-v2>
    <el-button @click="set2">设置</el-button>
    <el-button @click="clear2">清空</el-button>
    <p>{{ value2 }}</p>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const initials = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']
const value1 = ref('')
const value2 = ref([])
const options = Array.from({ length: 1000 }).map((_, idx) => ({
  value: `Option ${idx + 1}`,
  label: `${initials[idx % 10]}${idx}`,
}))
const set1 = () => {
  value1.value = 'Option 1'
}
function clear1() {
  value1.value = ''
}
const set2 = () => {
  value2.value = ['Option 1']
}
function clear2() {
  value2.value = []
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
