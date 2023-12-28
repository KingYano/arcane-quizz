<template>
  <main class="main">
    <div class="main__container">
        <div class="main__side-left">
            <button class="btn__play" v-on:click="$emit('play')">
                <span>Jouer</span>
            </button>
        </div>
        <div class="main__side-right">
            <SocialMedia></SocialMedia>
        </div>
    </div>
  </main>
</template>

<script setup lang="ts">
import SocialMedia from '../SocialMedia/SocialMedia.vue';

</script>

<style lang="scss">
    @import './MainSection.scss';
</style>
