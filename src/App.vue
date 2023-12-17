<template>
    <div class="background">
      <PageContainer></PageContainer>
    </div>
</template>

<script setup lang="ts">
  import PageContainer from './components/PageContainer/PageContainer.vue';
</script>

<style lang="scss">
  .background {
    width: 100vw;
    height: 100vh;
    display: flex;
    justify-content: center;
    align-items: center;
    background: url('./assets/background/background-desktop-blur_1.jpg') no-repeat;
    background-size: cover;
    background-position: right 20% top 1%;
  }
</style>
