<template>
  <div class="page-container" :class="{'page-container--hidden': !showMainSection}">
    <HeaderSection></HeaderSection>
    <MainSection v-if="showMainSection" @play="toggleSection"></MainSection>
    <QuizzQuestion v-if="!showMainSection"></QuizzQuestion>
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
