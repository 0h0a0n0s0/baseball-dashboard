<template>
  <section class="metrics-panel">
    <ul>
      <li v-for="item in metrics" :key="item.name">
        <span>{{ item.name }}</span>
        <span>{{ item.value }}</span>
      </li>
    </ul>
  </section>
</template>

<script setup>
import { ref } from 'vue'
const metrics = ref([
  { name: '站姿', value: 1 },
  { name: '平衡', value: 1 },
  { name: '手臂位置', value: 1 },
  { name: '腳步', value: 1 },
  { name: '時機掌握', value: 1 },
])
</script>

<style scoped>
.metrics-panel {
  flex: 2;
  overflow-y: auto;
  padding: 1rem;
}
.metrics-panel ul {
  list-style: none;
  padding: 0;
  margin: 0;
}
.metrics-panel li {
  display: flex;
  justify-content: space-between;
  padding: 0.5rem 0;
  border-bottom: 1px solid #eee;
}
</style>
