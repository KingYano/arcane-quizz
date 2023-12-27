<template>
  <main class="main">
    <div class="main__container">
        <div class="main__side-left">
            <button class="btn__play">
                Jouer
            </button>
        </div>
        <div class="main__side-right">
            <SocialMedia></SocialMedia>
            <QuizzProgression></QuizzProgression>
        </div>
    </div>
  </main>
</template>

<script setup lang="ts">
import SocialMedia from '../SocialMedia/SocialMedia.vue';
import QuizzProgression from '../QuizzProgression/QuizzProgression.vue';

</script>

<style lang="scss">
    @import './MainSection.scss'
</style>
