<template>
  <div class="page-container" :class="{'page-container--hidden': !showMainSection}">
    <HeaderSection></HeaderSection>
    <MainSection v-if="showMainSection" @play="toggleSection"></MainSection>
    <QuizzQuestion v-if="!showMainSection"></QuizzQuestion>
    <div class="quizz-right">
      <a class="logo-riot" href="https://www.riotgames.com/fr" aria-label="Ouvrir le site Riot Games">
        <img src="@/assets/logo/logo_riot.svg" aria-hidden="true" target="_blank" alt="logo Riot Games">
      </a>
      <div class="quizz-riot-right">
        <p>© 2024 Riot Games, Inc. ARCANE LEAGUE OF LEGENDS, marques déposées de Riot Games, Inc.</p>
        <p>© Yanis Belkadi 2024.</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
  import HeaderSection from '../HeaderSection/HeaderSection.vue';
  import MainSection from '../MainSection/MainSection.vue';
  import QuizzQuestion from '../QuizzQuestion/QuizzQuestion.vue';

  import { ref } from 'vue';

  const showMainSection = ref(true);

  const toggleSection = () => {
    showMainSection.value = !showMainSection.value;
  };

</script>

<style lang="scss">
    @import './PageContainer.scss';
</style>
