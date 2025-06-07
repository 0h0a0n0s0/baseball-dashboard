<template>
  <nav class="menu-tabs">
    <button>風險指標</button>
    <button>歷史紀錄</button>
    <button>改善建議</button>
  </nav>
</template>

<script setup></script>

<style scoped>
.menu-tabs {
  display: flex;
  border-bottom: 1px solid #ccc;
  background: #fafafa;
}
.menu-tabs button {
  padding: 0.5rem 1rem;
  border: none;
  background: transparent;
  cursor: pointer;
}
.menu-tabs button:hover {
  background: #eee;
}
</style>
