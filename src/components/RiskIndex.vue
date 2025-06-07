<template>
  <section class="risk-index">
    <div class="gauge">55</div>
  </section>
</template>

<script setup></script>

<style scoped>
.risk-index {
  flex: 1;
  display: flex;
  align-items: center;
  justify-content: center;
  border-bottom: 1px solid #ccc;
  padding: 1rem;
}
.gauge {
  font-size: 2rem;
  color: red;
}
</style>
