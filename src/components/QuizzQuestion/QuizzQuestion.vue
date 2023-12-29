<template>
  <main class="main-question">
    <div class="quizz-container">
      <div class="quizz-progression">
        <QuizzProgression></QuizzProgression>
      </div>
      <div class="quizz-texte">
        <h3>{{ questions[currentQuestionIndex].question }}</h3>
      </div>
      <div class="quizz-response">
        <div v-for="(answer, index) in questions[currentQuestionIndex].answers"
             :key="index"
             :class="getClass(answer)"
             @click="selectAnswer(answer)">
          {{ answer }}
        </div>
      </div>
      <button v-if="isAnswerSubmitted" @click="goToNextQuestion">Suivant</button>
    </div>
  </main>
</template>


<script setup lang="ts">
  import { ref } from 'vue';
  import QuizzProgression from '../QuizzProgression/QuizzProgression.vue';
  import { questions } from '@/components/QuizzQuestion/data/questionsData';

  const currentQuestionIndex = ref<number>(0);
  const selectedAnswer = ref<string>("");
  const isAnswerSubmitted = ref<boolean>(false);

  const selectAnswer = (answer: string) => {
    if (isAnswerSubmitted.value) {
      return;
    }

    selectedAnswer.value = answer;
    isAnswerSubmitted.value = true;
  };


  const goToNextQuestion = () => {
    if (currentQuestionIndex.value < questions.length - 1) {
      currentQuestionIndex.value++;
      selectedAnswer.value = "";
      isAnswerSubmitted.value = false;
    } else {
      console.log('fin du quizz !');
    }
  };

  const getClass = (answer: string) => {
    if (!isAnswerSubmitted.value) return '';

    if (answer === questions[currentQuestionIndex.value].correctAnswer) {
      return 'correct';
    } else if (answer === selectedAnswer.value) {
      return 'incorrect';
    }

    return '';
  };



</script>

<style lang="scss">
    @import './QuizzQuestion.scss';

    .correct {
      background-color: green;
    }

    .incorrect {
      background-color: red;
    }
</style>
