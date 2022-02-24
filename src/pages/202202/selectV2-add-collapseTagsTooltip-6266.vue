<template>
  <div style="display: inline-block">
    <p style="margin: 10px">default</p>
    <el-select-v2
        v-model="value"
        :options="options"
        placeholder="Please select"
        style="width: 240px"
        multiple
    />
  </div>
  <div style="display: inline-block; margin-left: 20px">
    <p style="margin: 10px">use collapse-tags</p>
    <el-select-v2
        v-model="value2"
        :options="options"
        placeholder="Please select"
        style="width: 240px"
        multiple
        collapse-tags
    />
  </div>
  <div style="display: inline-block; margin-left: 20px">
    <p style="margin: 10px">use collapse-tags-tooltip</p>
    <el-select-v2
        v-model="value3"
        :options="options"
        placeholder="Please select"
        style="width: 240px"
        multiple
        collapse-tags
        collapse-tags-tooltip
    />
  </div>
</template>

<script lang="ts" setup>
import { ref } from 'vue'
const initials = ['a', 'b', 'c', 'd', 'e', 'f', 'g', 'h', 'i', 'j']

const value = ref([
  'Option 1',
  'Option 2',
  'Option 3',
  'Option 4',
  'Option 5',
  'Option 11',
  'Option 21',
  'Option 31',
  'Option 41',
  'Option 51',
  'Option 12',
  'Option 22',
  'Option 32',
  'Option 42',
  'Option 52',
  'Option 13',
  'Option 23',
  'Option 33',
  'Option 43',
  'Option 53',
  'Option 14',
  'Option 24',
  'Option 34',
  'Option 44',
  'Option 54',
])
const value2 = ref([
  'Option 1',
  'Option 2',
  'Option 3',
  'Option 4',
  'Option 5',
  'Option 11',
  'Option 21',
  'Option 31',
  'Option 41',
  'Option 51',
  'Option 12',
  'Option 22',
  'Option 32',
  'Option 42',
  'Option 52',
  'Option 13',
  'Option 23',
  'Option 33',
  'Option 43',
  'Option 53',
  'Option 14',
  'Option 24',
  'Option 34',
  'Option 44',
  'Option 54',
])
const value3 = ref([
  'Option 1',
  'Option 2',
  'Option 3',
  'Option 4',
  'Option 5',
  'Option 11',
  'Option 21',
  'Option 31',
  'Option 41',
  'Option 51',
  'Option 12',
  'Option 22',
  'Option 32',
  'Option 42',
  'Option 52',
  'Option 13',
  'Option 23',
  'Option 33',
  'Option 43',
  'Option 53',
  'Option 14',
  'Option 24',
  'Option 34',
  'Option 44',
  'Option 54',
])
const options = Array.from({ length: 1000 }).map((_, idx) => ({
  value: `Option ${idx + 1}`,
  label: `${initials[idx % 10]}${idx}`,
}))
</script>
