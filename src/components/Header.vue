<template>
  <header class="header">
    <div class="logo">
      <img :src="logoPath" alt="Logo" class="logo-img" />
    </div>
    <div class="title">
      <h1>棒球姿勢分析儀表板</h1>
      <p>即時動作分析與技術改善建議</p>
    </div>
    <div class="controls">
      <div>比賽日期: <input type="date" /></div>
      <div>比賽對手: <select><option>台中棒球隊</option></select></div>
      <PlayerInfo
        :image-path="playerImage"
        :player-name="playerName"
        :handedness="handedness"
        :pitches="pitches"
        @switch="onSwitchPlayer"
        @more="onViewMore"
      />
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue'
import playerImage from '../assets/profile_photo_1.jpeg'
import PlayerInfo from './PlayerInfo.vue'

// 範例資料，之後可改成從 API 拿
const playerName = ref('茂野吾郎')
const handedness = ref('右手')
const pitches = ref(['1號球', '2號球', '3號球'])

// 這裡觸發切換球員的流程
function onSwitchPlayer() {
  console.log('切換球員')
}

// 這裡顯示更多資料
function onViewMore() {
  console.log('查看更多')
}
// 註冊子元件
</script>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  flex-wrap: wrap;            /* 確保窄螢幕時會換行 */
  padding: 1rem;
  box-sizing: border-box;
  width: 100%;
}
.controls {
  display: flex;
  align-items: center;
  flex: 1;                    /* 讓 controls 區塊拉伸佔滿中間空間 */
  flex-wrap: wrap;
  margin-left: 2rem;          /* title 右邊留點空間 */
}
.controls > div {
  margin-right: 1rem;         /* 各欄位水平間距 */
}
.player-info {
  margin-left: auto;          /* 自動推到最右 */
  display: flex;
  align-items: center;
}
.logo {
  /* 既有：width / height / background 等 */
  width: 80px;
  height: 40px;
}
.logo-img {
  width: 100%;
  height: 100%;
  object-fit: contain;
}
</style>

