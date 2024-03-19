<template>
  <div 
    :class="{
      'player-menu-container': true,
      'player-menu-container-show': show
    }"
    
  >
    Player Menu
  </div>
</template>

<script setup lang="ts">
import { watch } from 'vue';


const show = defineModel<boolean>('show', { default: false });

watch(
  show,
  (nv) => {
    console.log('show', nv);
  },
  {
    immediate: true
  }
);
// defineProps<{

// }>();


</script>

<style scoped>
.player-menu-container {
  position: fixed;
  bottom: 0;
  right: 0;
  height: 0;
  width: 100%;
  z-index: 1000;
  background-color: var(--primary-color);
  border: none;
  transition: all 0.3s ease-in-out;
}

.player-menu-container-show {
  height: 96px;
}
</style>