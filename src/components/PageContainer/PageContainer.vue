<template>
  <div class="page-container">
    <HeaderSection></HeaderSection>
    <MainSection></MainSection>
  </div>
</template>

<script setup lang="ts">
  import HeaderSection from '../HeaderSection/HeaderSection.vue';
  import MainSection from '../MainSection/MainSection.vue';
</script>

<style lang="scss">
    @import './PageContainer.scss';
</style>
