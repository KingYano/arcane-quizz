<template>
  <div class="progression-container">
    <div class="progression">
      <span class="bubble"
            v-for="(bubble, index) in bubblesRef"
            :key="bubble.id"
            :class="{
              'bubble--correct': computedQuestionStatus[index] === 'correct',
              'bubble--incorrect': computedQuestionStatus[index] === 'incorrect'
            }">
        {{ bubble.number }}
      </span>
    </div>
  </div>
</template>

<script setup lang="ts">
  import { ref, defineProps, computed } from 'vue';
  import { bubbles } from '@/components/QuizzProgression/data/bubblesData';

  const bubblesRef = ref(bubbles);

  const props = defineProps({
    questionStatus: {
      type: Array,
      default: () => []
    }
  });

  const computedQuestionStatus = computed(() => {
    return props.questionStatus ?? [];
  });
</script>

<style lang="scss">
  @import './QuizzProgression.scss';
</style>
