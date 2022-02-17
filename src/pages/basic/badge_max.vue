<template>
  <el-badge :value="200" :max="99" class="item">
    <el-button size="small">comments</el-button>
  </el-badge>
  <el-badge :value="100" :max="10" class="item">
    <el-button size="small">replies</el-button>
  </el-badge>
</template>

<script>
export default {
  name: "badge_max",
};
</script>

<style scoped></style>
