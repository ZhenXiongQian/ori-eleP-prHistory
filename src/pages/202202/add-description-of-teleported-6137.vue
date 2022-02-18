<template>
  <div style="margin-bottom: 100px">
    <el-popover placement="bottom" :width="200" trigger="click">
      <template #reference>
        <el-button>Click to pop</el-button>
      </template>
      <el-select
        v-model="selectedItems"
        :teleported="false"
        placeholder="example1"
      >
        <el-option
          v-for="item in items"
          :key="item.value"
          :label="item.label"
          :value="item.value"
        />
      </el-select>
      <el-popover
        :teleported="false"
        placement="bottom"
        :width="200"
        content="click me"
      >
        <template #reference>
          <el-button>example2</el-button>
        </template>
      </el-popover>
    </el-popover>
  </div>
  <div style="margin-bottom: 100px">
    <el-popover placement="bottom" :width="250" trigger="click">
      <template #reference>
        <el-button>Click to pop2</el-button>
      </template>
      <el-date-picker
        v-model="date"
        :teleported="false"
        type="date"
        placeholder="example3"
      />
    </el-popover>
    <span style="margin-left: 20px">Date Picker seems to be fine.</span>
  </div>
  <div style="margin-bottom: 100px">
    <el-popover placement="bottom" :width="200" trigger="click">
      <el-date-picker
        v-model="value1"
        :teleported="false"
        type="daterange"
        range-separator="To"
        start-placeholder="Start date"
        end-placeholder="End date"
      >
      </el-date-picker>
      <template #reference>
        <el-button>Hover to activate</el-button>
      </template>
    </el-popover>
  </div>
  <div style="margin-bottom: 100px">
    <el-popover placement="bottom" :width="200" trigger="click">
      <el-date-picker
        v-model="value2"
        :teleported="false"
        type="datetime"
        placeholder="Select date and time"
      >
      </el-date-picker>
      <template #reference>
        <el-button>Hover to activate</el-button>
      </template>
    </el-popover>
  </div>
  <div style="margin-bottom: 100px">
    <el-popover placement="bottom" :width="200" trigger="click">
      <el-time-picker
        v-model="value3"
        :teleported="false"
        placeholder="Arbitrary time"
      >
      </el-time-picker>
      <template #reference>
        <el-button>Hover to activate</el-button>
      </template>
    </el-popover>
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  setup() {
    return {
      items: [
        { label: "one", value: 1 },
        { label: "two", value: 2 },
        { label: "three", value: 3 },
      ],
      selectedItems: ref([]),
      date: ref(""),
      value1: ref([]),
      value2: ref(""),
      value3: ref(),
    };
  },
};
</script>
