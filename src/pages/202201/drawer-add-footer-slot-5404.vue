<template>
  <el-radio-group v-model="direction">
    <el-radio label="ltr">left to right</el-radio>
    <el-radio label="rtl">right to left</el-radio>
    <el-radio label="ttb">top to bottom</el-radio>
    <el-radio label="btt">bottom to top</el-radio>
  </el-radio-group>

  <el-button type="primary" style="margin-left: 16px" @click="drawer = true">
    open
  </el-button>

  <el-drawer v-model="drawer" title="I am the title" :direction="direction">
    <template #title>
      <h4>set title by slot</h4>
    </template>
    <template #default>
      <p>set default slot</p>
    </template>
    <template #footer>
      <div style="flex: auto">
        <el-button>cancel</el-button>
        <el-button type="primary">confirm</el-button>
      </div>
    </template>
  </el-drawer>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const drawer = ref(false);
const direction = ref("rtl");
</script>
