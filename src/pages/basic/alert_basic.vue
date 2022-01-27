<template>
  <el-alert title="unclosable alert" type="success" :closable="false">
  </el-alert>
  <el-alert title="customized close-text" type="info" close-text="Gotcha">
  </el-alert>
  <el-alert title="alert with callback" type="warning" @close="hello">
  </el-alert>
</template>

<script>
export default {
  name: "alert_basic",
};
</script>

<style scoped></style>
