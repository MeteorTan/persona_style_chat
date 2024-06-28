<template>
  <div :class="['dialogue_layout', props.isMe ? 'right-to-left' : 'left-to-right']">
    <div class="dialogue_icon"></div>
    <img src="../assets/arrow.svg" :class="['dialogue_arrow', props.isMe ? 'arrow_to_me' : '']" />
    <div class="dialogue_border">
      <div class="content_background">
        {{ props.content }}
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { defineProps } from 'vue'
const props = defineProps(['isMe', 'content'])
</script>

<style scoped>
.dialogue_layout {
  display: flex;
  align-items: center;
}

.left-to-right {
  flex-direction: row;
}

.right-to-left {
  flex-direction: row-reverse;
}

.dialogue_border {
  display: flex;
  justify-items: center;
  padding: 10px;
  background: white;
  margin-top: 20px;
}

.dialogue_arrow {
  width: 100px;
  height: 80px;
  background: transparent;
}

.arrow_to_me {
  transform: rotateY(180deg);
}

.dialogue_icon {
  width: 100px;
  height: 80px;
  background: black;
}

.content_background {
  width: auto;
  height: 80px;
  background: black;
  color: white;
}
</style>