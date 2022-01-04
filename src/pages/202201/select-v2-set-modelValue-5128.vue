<template>
  <el-select-v2
    v-model="value"
    :options="options"
    :multiple="true"
    placeholder="Please select"
    style="width: 200px"
    size="large"
  ></el-select-v2>
  <el-button @click="set">设置</el-button>
  <el-button @click="clear">清空</el-button>
  <p>{{ value }}</p>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";
export default defineComponent({
  setup() {
    const initials = ["a", "b", "c", "d", "e", "f", "g", "h", "i", "j"];
    const value = ref([]);
    const options = Array.from({ length: 1000 }).map((_, idx) => ({
      value: `Option ${idx + 1}`,
      label: `${initials[idx % 10]}${idx}`,
    }));

    const set = () => {
      value.value = ["Option 1"];
    };
    function clear() {
      value.value = [];
    }
    return {
      initials,
      value,
      options,
      set,
      clear,
    };
  },
});
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
