<template>
  <el-avatar :size="60" src="https://empty" @error="errorHandler">
    <img
      src="https://cube.elemecdn.com/e/fd/0fc7d20532fdaf769a25683617711png.png"
    />
  </el-avatar>
</template>

<script setup lang="ts">
const errorHandler = () => true;
</script>

<style scoped></style>
