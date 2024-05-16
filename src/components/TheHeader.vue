<script setup lang="ts">
const links = [
  {
    name: 'Program',
    path: 'program',
  },
  {
    name: 'Participants',
    path: 'participants',
  },
  {
    name: 'Media',
    path: 'media',
  },
]
</script>

<template>
  <header class="header">
    <div class="container header__container">
      <router-link to="/">
        <img class="header__logo" src="/src/assets/images/logo.svg" alt="" />
      </router-link>
      <nav class="navbar">
        <ul class="navbar__list">
          <li v-for="link in links" :key="link.path" class="navbar__item">
            <router-link :to="link.path">{{ link.name }}</router-link>
          </li>
        </ul>
        <div class="header__btn-wrapper">
          <button>EN</button>
          <a href="#">Register</a>
        </div>
      </nav>
    </div>
  </header>
</template>

<style scoped>
.header__container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header__logo {
  width: 60px;
  height: 60px;
  display: flex;
}
</style>
