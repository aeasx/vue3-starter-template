<script setup lang="ts">
import { ref } from 'vue'

const arr = ref(Array.from({ length: 5 }, (_, i) => i + 1))
function handleObserver() {
  arr.value = arr.value.map(item => item.valueOf() * 2 + 1)
}
</script>

<template>
  <h1>AboutView</h1>
  <div>
    <ul>
      <li v-for="value in arr" :key="value">
        {{ value }}
      </li>
    </ul>
    <el-button @click="handleObserver">
      Observer
    </el-button>
  </div>
</template>
