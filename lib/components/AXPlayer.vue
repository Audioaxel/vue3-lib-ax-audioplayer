<script setup lang="ts">
import { ref } from 'vue';
import AXPlayerMenu from './parts/AXPlayerMenu.vue';
import AXMainButton from './parts/AXMainButton.vue';

const showPlayerMenu = ref(false);

</script>

<template>
  <AXMainButton @click="showPlayerMenu = !showPlayerMenu;">
    <template #icon>
      <slot name="icon" />
    </template>
  </AXMainButton>
  <AXPlayerMenu
    v-model:show="showPlayerMenu"
  >
    
  </AXPlayerMenu>
</template>