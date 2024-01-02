<template>
  <main>
    <div v-if="!quizFinished" class="main-question" :style="backgroundStyle">
      <div class="quizz-container">
        <div class="quizz-progression">
          <QuizzProgression :questionStatus="questionStatus"></QuizzProgression>
        </div>
        <div class="quizz-texte">
          <h3>{{ questions[currentQuestionIndex].question }}</h3>
        </div>
        <div class="quizz-container-responses">
          <div class="quizz-choise-responses">
            <button class="quizz-response" v-for="(answer, index) in questions[currentQuestionIndex].answers"
                    :key="index"
                    :class="addingClassAnswer(answer)"
                    @click="selectAnswer(answer)">
              {{ answer }}
            </button>
          </div>
        </div>
        <div class="quizz-command">
          <button class="quizz-next-button" v-if="isAnswerSubmitted" @click="goToNextQuestion">Suivant</button>
        </div>
      </div>
    </div>
    <div class="main-result" v-else>
      <QuizzResult :score="calculateScore()"></QuizzResult>
    </div>
  </main>
</template>

<script setup lang="ts">
  import { ref, computed } from 'vue';
  import QuizzProgression from '../QuizzProgression/QuizzProgression.vue';
  import QuizzResult from '../QuizzResult/QuizzResult.vue';
  import { questions } from '@/components/QuizzQuestion/data/questionsData';

  const currentQuestionIndex = ref<number>(0);
  const selectedAnswer = ref<string>("");
  const isAnswerSubmitted = ref<boolean>(false);
  const quizFinished = ref<boolean>(false);
  const questionStatus = ref<Array<'correct' | 'incorrect' | 'unanswered'>>(new Array(questions.length).fill('unanswered'));

  const selectAnswer = async (answer: string) => {
    if (isAnswerSubmitted.value) {
      return;
    }
    selectedAnswer.value = answer;
    isAnswerSubmitted.value = true;

    if (answer === questions[currentQuestionIndex.value].correctAnswer) {
      questionStatus.value[currentQuestionIndex.value] = 'correct';
    } else {
      questionStatus.value[currentQuestionIndex.value] = 'incorrect';
    }
  };

  const goToNextQuestion = () => {
    if (currentQuestionIndex.value < questions.length - 1) {
      currentQuestionIndex.value++;
      selectedAnswer.value = "";
      isAnswerSubmitted.value = false;
    } else {
      quizFinished.value = true;
    }
  };

  const calculateScore = () => {
    return questionStatus.value.filter(status => status === 'correct').length;
  };

  const addingClassAnswer = (answer: string) => {
    if (!isAnswerSubmitted.value) return '';

    if (answer === questions[currentQuestionIndex.value].correctAnswer) {
      return 'quizz-response--correct';
    } else if (answer === selectedAnswer.value) {
      return 'quizz-response--incorrect';
    }
    return '';
  };

  const backgroundStyle = computed(() => {
    return {
      background: `url(./../${questions[currentQuestionIndex.value].imagePath}) no-repeat`
    };
  });
</script>

<style lang="scss">
  @import './QuizzQuestion.scss';
</style>
