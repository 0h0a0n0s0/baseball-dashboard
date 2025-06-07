<template>
  <div id="app">
    <Header />
    <MenuTabs />
    <div class="content">
      <VideoSection />
      <div class="right-panel">
        <RiskIndex />
        <MetricsPanel />
      </div>
    </div>
    <Footer />
  </div>
</template>

<script setup>
import Header from './components/Header.vue'
import MenuTabs from './components/MenuTabs.vue'
import VideoSection from './components/VideoSection.vue'
import RiskIndex from './components/RiskIndex.vue'
import MetricsPanel from './components/MetricsPanel.vue'
import Footer from './components/Footer.vue'
</script>

<style>
#app {
  display: flex;
  flex-direction: column;
  min-height: 100vh;
  width: 100%;             /* 滿版寬度 */
  box-sizing: border-box;   /* 包括 padding 在內 */
  padding: 0;               /* 如果要左右留白，可改成 e.g. 0 1rem */
}
.content {
  flex: 1;
  display: flex;
  flex-wrap: wrap;          /* 窄螢幕時會自動斷行 */
}
.right-panel {
  flex: 1;
  display: flex;
  flex-direction: column;
}
</style>

