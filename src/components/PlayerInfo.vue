<template>
  <div class="player-info">
    <img
      :src="playerImage"
      alt="球員頭像"
      class="avatar"
    />
    <div class="info">
      <div class="name-switch">
        <span class="name">{{ playerName }}</span>
        <button class="switch-btn" @click="onSwitch">
          切換球員
        </button>
      </div>
      <div class="details">
        <span>慣用手: {{ handedness }}</span>
        <span>球種: {{ pitches.join('、') }}</span>
      </div>
      <a href="#" class="more" @click.prevent="onMore">
        更多...
      </a>
    </div>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from 'vue'

const props = defineProps({
  imagePath: { type: String, required: true },
  playerName: { type: String, required: true },
  handedness: { type: String, default: '右手' },
  pitches: {
    type: Array,
    default: () => ['1號球', '2號球', '3號球']
  }
})

const emit = defineEmits(['switch', 'more'])

function onSwitch() {
  emit('switch')
}
function onMore() {
  emit('more')
}
</script>

<style scoped>
.player-info {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  padding: 0.5rem;
  border: 1px solid #ddd;
  border-radius: 4px;
}

.avatar {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  object-fit: cover;
}

.info {
  display: flex;
  flex-direction: column;
  gap: 0.25rem;
}

.name-switch {
  display: flex;
  align-items: center;
  gap: 0.5rem;
}

.name {
  font-weight: bold;
}

.switch-btn {
  padding: 0.25rem 0.5rem;
  border: 1px solid #888;
  background: white;
  cursor: pointer;
  border-radius: 3px;
}
.switch-btn:hover {
  background: #f0f0f0;
}

.details {
  font-size: 0.875rem;
  color: #555;
  display: flex;
  gap: 1rem;
}

.more {
  font-size: 0.875rem;
  color: #0366d6;
  text-decoration: none;
  cursor: pointer;
  margin-top: 0.25rem;
}
.more:hover {
  text-decoration: underline;
}
</style>
