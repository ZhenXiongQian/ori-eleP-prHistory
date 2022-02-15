<template>
  <el-row :gutter="12" class="demo-radius">
    <el-col
      v-for="(radius, i) in radiusGroup"
      :key="i"
      :span="6"
      :xs="{ span: 12 }"
    >
      <div class="title">{{ radius.name }}</div>
      <div class="value">
        <code>border-radius: {{ getValue(radius.type) || "0px" }}</code>
      </div>
      <div
        class="radius"
        :style="{
          borderRadius: radius.type
            ? `var(--el-border-radius-${radius.type})`
            : '',
        }"
      ></div>
    </el-col>
  </el-row>
</template>

<script setup lang="ts">
import { ref } from "vue";

radiusGroup: ref([
  {
    name: "No Radius",
    type: "",
  },
  {
    name: "Small Radius",
    type: "small",
  },
  {
    name: "Large Radius",
    type: "base",
  },
  {
    name: "Round Radius",
    type: "round",
  },
]);

function getValue(type: any) {
  const getCssVarValue = (prefix: string, type: any) =>
    getComputedStyle(document.documentElement).getPropertyValue(
      `--el-${prefix}-${type}`
    );
  return getCssVarValue("border-radius", type);
}
</script>
