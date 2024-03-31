<template>
  <header class="header">
    <nav class="navigation">
      <img src="../assets/images/INVITE.svg" alt="Электронное приглашение"/>
      <h2 class="visually-hidden">Навигационное меню</h2>
      <div class="burger" @click="toggleMenu">
        <div class="burger__field" id="burger">
          <span class="burger__bar"></span>
          <span class="burger__bar"></span>
          <span class="burger__bar"></span>
        </div>
      </div>
    </nav>
    <div class="navigation__menu" :class="{ 'open': isMenuOpen }" id="navigation__menu">
      <div class="navigation__list">
        <a v-for="item in items" :key="item.message" class="navigation__link" :href="'#' + item.id" @click="handleNavigationClick">{{ item.message }}</a>
      </div>
    </div>
  </header>
</template>

<script setup>
import { ref } from 'vue';

const items = [
  { message: "Место и дата", id: "place-and-date"},
  { message: "Тайминг", id: "timing"},
  { message: "Детали", id: "details"},
  { message: "Вопросы", id: "questions"}
];

const isMenuOpen = ref(false);

function toggleMenu() {
  isMenuOpen.value = !isMenuOpen.value;
  const burgerField = document.getElementById('burger');
  if (isMenuOpen.value) {
    burgerField.classList.add('active');
  } else {
    burgerField.classList.remove('active');
  }
}

function handleNavigationClick() {
  isMenuOpen.value = false;
}
</script>

<style lang="scss" scoped>
header {
  background-color: #d3d3d3;
  padding-top: 85px;
}

a {
  font-size: 19px;
  line-height: 30px;
}

.navigation {
  position: fixed;
  left: 0;
  top: 0;
  padding-top: 15px;
  padding-bottom: 10px;
  padding-left: 15px;
  width: 100%;
  background-color: #d3d3d3;
  z-index: 1000;

  display: flex;
  justify-content: space-between;

  &__list {
    display: none;
    flex-direction: column;
    text-transform: uppercase;
    text-decoration: underline;
  }

  &__link {
    padding: 15px;
    text-decoration: none;
    color: #333333;
  }

  &__menu {
    position: fixed;
    top: 85px;
    right: -100%;
    width: 100%;
    height: 100%;
    background-color: #fff;
    z-index: 100;
    display: flex;
    transition: 0.3s;
  }

  &__menu.open {
    right: 0;
  }

  &__menu .navigation__list {
    width: 100%;
    height: 100%;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: start;
    padding: 10px 0;
    overflow: auto;
  }

  .navigation__menu .navigation__list > a {
    width: 100%;
  }

  body.noscroll {
    overflow: hidden;
  }

  img {
    width: 238px;
  }
}

.burger {
    display: flex;
    align-items: center;
    position: relative;
    right: 15px;
  }

.burger__field {
    padding: 15px 15px;
    cursor: pointer;
  }

.burger__bar {
  display: block;
  width: 30px;
  height: 2px;
  margin: 6px auto;
  background-color: black;
  transition: 0.2s;
}

.burger__field.active .burger__bar:nth-child(2) {
  opacity: 0;
}

.burger__field.active .burger__bar:nth-child(1) {
  transform: translateY(8px) rotate(45deg);
}

.burger__field.active .burger__bar:nth-child(3) {
  transform: translateY(-8px) rotate(-45deg);
}

@media(min-width: 768px) {
  .navigation {
    padding-left: 30px;
    padding-right: 15px;
  }

  img {
    width: 345px;
  }

  .burger {
    right: 45px;
  }
}

</style>