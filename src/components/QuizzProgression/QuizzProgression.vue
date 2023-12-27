<template>
  <div class="progression-container">
    <div class="progression">
      <span class="bubble" v-for="bubble in bubbles" :key="bubble.id">{{ bubble.number }}</span>
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';

interface Bubble {
  id: number;
  number: string;
}

const bubbles = ref<Bubble[]>([
  { id: 1, number: '1' },
  { id: 2, number: '2' },
  { id: 3, number: '3' },
  { id: 4, number: '4' },
  { id: 5, number: '5' },
  { id: 6, number: '6' },
  { id: 7, number: '7' },
  { id: 8, number: '8' },
]);
</script>

<style lang="scss">
    @import './QuizzProgression.scss';
</style>

