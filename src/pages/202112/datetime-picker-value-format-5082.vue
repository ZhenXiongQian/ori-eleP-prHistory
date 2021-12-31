<template>
  <div className="demo-date-picker">
    <div className="block">
      <span className="demonstration">Emits Date object</span>
      <div className="demonstration">Value: {{ value1 }}</div>
      <el-date-picker
        v-model="value1"
        type="datetime"
        placeholder="Pick a Date"
        format="YYYY/MM/DD hh:mm:ss"
      >
      </el-date-picker>
    </div>
    <div className="block">
      <span className="demonstration">Use value-format</span>
      <div className="demonstration">Value：{{ value2 }}</div>
      <el-date-picker
        v-model="value2"
        type="datetime"
        placeholder="Pick a Date"
        format="YYYY/MM/DD hh:mm:ss"
        value-format="YYYY-MM-DD h:m:s a"
      >
      </el-date-picker>
    </div>
    <div className="block">
      <span className="demonstration">Timestamp</span>
      <div className="demonstration">Value：{{ value3 }}</div>
      <el-date-picker
        v-model="value3"
        type="datetime"
        placeholder="Pick a Date"
        format="YYYY/MM/DD hh:mm:ss"
        value-format="x"
      >
      </el-date-picker>
    </div>
  </div>
</template>

<script lang="ts">
import { defineComponent, ref } from "vue";

export default defineComponent({
  setup() {
    const value1 = ref("");
    const value2 = ref("");
    const value3 = ref("");

    return {
      value1,
      value2,
      value3,
    };
  },
});
</script>

<style>
.example-showcase .demo-date-picker {
  display: flex;
  width: 100%;
  padding: 0;
  flex-wrap: wrap;
}

.demo-date-picker .block {
  padding: 30px 0;
  text-align: center;
  flex: 1;
  &:last-child {
    border-right: none;
  }
}

.demo-date-picker .container {
  flex: 1;
  border-right: solid 1px var(--el-border-color-base);
  .block {
    border-right: none;
    &:last-child {
      border-top: solid 1px var(--el-border-color-base);
    }
  }
  &:last-child {
    border-right: none;
  }
}

.demo-date-picker .demonstration {
  display: block;
  color: var(--el-text-color-secondary);
  font-size: 14px;
  margin-bottom: 20px;
}
</style>
