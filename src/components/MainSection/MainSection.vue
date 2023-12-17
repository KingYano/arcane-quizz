<template>
  <main class="main">
    <div class="main__container">
        <div class="main__side-left">
            <button>
                jouer
            </button>
        </div>
        <div class="main__side-right">
            <SocialMediaDesktop></SocialMediaDesktop>
        </div>
    </div>
  </main>
</template>

<script setup lang="ts">
  import SocialMediaDesktop from '../SocialMedia/SocialMediaDesktop.vue';

</script>

<style lang="scss">
    .main {
        height: calc(100% - 111px);
        border-bottom-left-radius: var(--big-border-radius) ;
        border-bottom-right-radius: var(--big-border-radius) ;
        // background: var(--background-primary-color);
        // background: url('./../../assets/images/image_1.jpg') no-repeat;
        background-size: cover;
    }
</style>
