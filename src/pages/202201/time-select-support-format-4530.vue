<template>
  <el-time-select
    v-model="value"
    start="00:00"
    step="00:30"
    end="23:59"
    placeholder="Select time"
  >
  </el-time-select>
  <p>{{ value }}</p>
  <el-time-select
    v-model="value2"
    start="00:00"
    step="00:30"
    end="23:30"
    format="hh:mm A"
    placeholder="Select time"
  >
  </el-time-select>
  <p>{{ value2 }}</p>
  <div class="demo-time-range">
    <el-time-select
      v-model="startTime"
      :max-time="endTime"
      placeholder="Start time"
      start="08:30"
      step="00:15"
      end="18:30"
      format="hh:mm a"
    >
    </el-time-select>
    <el-time-select
      v-model="endTime"
      :min-time="startTime"
      placeholder="End time"
      start="08:30"
      step="00:15"
      end="18:30"
      format="hh:mm a"
    >
    </el-time-select>
  </div>
  <el-button @click="t()">test</el-button>
</template>

<script setup lang="ts">
import { ref } from "vue";
// code here
const value = ref("");
const value2 = ref("");
const startTime = ref("");
const endTime = ref("");
const t = () => {
  startTime.value = "019:00";
};
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
.demo-time-range {
  .el-select {
    margin-right: 8px;
  }
}
</style>
