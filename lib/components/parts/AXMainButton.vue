<template>
  <span class="player-icon-container" @click="$emit('click')">
    <div class="player-icon">
      <AXContentCenter>
        <slot name="icon" />
      </AXContentCenter>
    </div>
  </span>
</template>

<script setup lang="ts">
import { AXContentCenter } from 'vue3-lib-ax-basics';

// defineProps<{
//   // backgoundColor
//   // size
//   // position
// }>();

defineEmits<{
  (name: 'click' ): void;
}>();

</script>

<style scoped>
.player-icon-container {
  position: fixed;
  bottom: 2vh;
  right: 2vw;
  height: 128px;
  width: 128px;
  z-index: 1001;
  background-color: var(--primary-color);
  opacity: 1;
  border-radius: 50%;
  border: none;
  transition: all 0.3s ease-in-out;
  cursor: pointer;
}
</style>