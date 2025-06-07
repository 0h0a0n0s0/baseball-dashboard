<template>
  <section class="video-section">
    <div class="video-container">
      <div class="placeholder">即時視訊</div>
    </div>
    <div class="video-controls">
      <button>開始錄製分析</button>
      <button>取消</button>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
.video-section {
  flex: 2;
  display: flex;
  flex-direction: column;
  padding: 1rem;
}
.video-container {
  flex: 1;
  border: 1px solid #000;
  display: flex;
  align-items: center;
  justify-content: center;
}
.video-controls {
  margin-top: 1rem;
}
.video-controls button {
  margin-right: 1rem;
  padding: 0.5rem 1rem;
}
</style>
