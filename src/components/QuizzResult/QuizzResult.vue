<template>
  <div class="quizz-result">
    <h2 class="quizz-result-score">Votre Score : {{ score }}/8</h2>
    <p class="quizz-result--message">{{ resultMessage }}</p>
  </div>
</template>

<script setup lang="ts">
import {computed, defineProps} from 'vue';

const props = defineProps({
  score: {
    type: Number,
    required: true
  }
});

const resultMessage = computed(() => {
  if (props.score === 8) {
    return "Félicitations ! Vous êtes un véritable expert d'Arcane !";
  } else if (props.score >= 4 && props.score <= 6) {
    return "Bien joué ! Vous connaissez bien Arcane, mais il y a encore un peu à apprendre.";
  } else if (props.score >= 1 && props.score <= 3) {
    return "Pas mal mais vous pouvez mieux faire. Pourquoi ne pas regarder à nouveau la série ?";
  } else {
    return "Oups ! Il semble que vous ayez besoin de rafraîchir vos connaissances sur la série Arcane.";
  }
});
</script>

<style>
  @import './QuizzResult.scss';
</style>
