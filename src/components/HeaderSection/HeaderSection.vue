<template>
    <header class="header">
        <div class="header__container">
          <div class="header__option" @click="toggleMenu">
            <i class="ri-menu-fill icone"></i>
          </div>
          <div class="dropdown-menu" v-show="isMenuOpen">
            <div class="menu-header">
              <i class="ri-close-fill" @click="toggleMenu"></i>
            </div>
            <hr class="separator"/>
            <ul class="menu-links">
              <li><a target="_blank" href="https://arcane.com/fr-fr/">Site Arcane</a></li>
              <li><a target="_blank" href="https://www.netflix.com/fr/title/81435684">Site Nextflix</a></li>
              <li><a target="_blank" href="https://www.riotgames.com/fr">Site Riot Games</a></li>
            </ul>
          </div>
          <div class="header__logo">
              <a target="_blank" href="https://arcane.com/fr-fr/">
                <img class="img" src="@/assets/logo/logo_arcane.svg" alt="logo de la série Arcane">
              </a>
          </div>
          <div class="header__redirection">
              <p class="subtitle">Disponible maintenant</p>
              <a target="_blank" href="https://www.netflix.com/fr/title/81435684">
                <img class="img" src="@/assets/logo/logo_netflix.svg" alt="logo Netflix">
              </a>
          </div>
        </div>
    </header>
</template>

<script setup lang="ts">
  import { ref } from 'vue';

  const isMenuOpen = ref(false);

  const toggleMenu = () => {
    isMenuOpen.value = !isMenuOpen.value;
  };
</script>

<style setup lang="scss">
    @import './HeaderSection.scss';
</style>
