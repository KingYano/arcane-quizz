<template>
  <div class="progression-container">
    <div class="progression">
      <span class="bubble" v-for="bubble in bubblesRef" :key="bubble.id">{{ bubble.number }}</span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
import { bubbles } from './Data/bubblesData';

const bubblesRef = ref(bubbles);
</script>

<style lang="scss">
@import './QuizzProgression.scss';
</style>
