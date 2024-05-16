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
      <router-link class="header__logo" to="/">
        <img class="header__logo-img" src="@/assets/images/logo.svg" alt="site logo" />
        <span
          >Third International Pharmaceutical
          <br />
          Forum of Uzbekistan
        </span>
      </router-link>
      <nav class="navbar">
        <ul class="navbar__list">
          <li v-for="link in links" :key="link.path" class="navbar__item">
            <router-link :to="link.path">{{ link.name }}</router-link>
          </li>
        </ul>
      </nav>
      <div class="header__btn-wrapper">
        <button class="main-btn lang-btn">
          <span>EN</span>
          <img src="@/assets/images/arrow-bottom.svg" alt="arrow bottom" />
        </button>
        <a class="main-btn header__register-btn" href="#">Register</a>
      </div>
    </div>
  </header>
</template>

<style scoped>
.header {
  padding-top: 30px;
  padding-bottom: 30px;
  background-color: #044636;
  color: #ffffff;
}

.header__container {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.header__logo {
  display: flex;
  align-items: center;
  font-size: 19px;
  font-weight: 500;
  line-height: 140%;
}

.header__logo-img {
  width: 60px;
  height: 60px;
  display: flex;
  margin-right: 8px;
}

.navbar__list {
  display: flex;
  align-items: center;
  gap: 40px;
  font-weight: 600;
}

.navbar__item {
  font-size: 20px;
  font-weight: 400;
  line-height: 150%;
  transition: all 0.2s ease;
}

.navbar__item:hover {
  color: #24cda5;
}

/* BTN */
.header__btn-wrapper {
  display: flex;
  align-items: center;
  gap: 16px;
}

.main-btn {
  display: flex;
  align-items: center;
  justify-content: center;
  border: none;
  border-radius: 20px;
  cursor: pointer;
  outline: none;
  padding: 14px 24px;
  font-size: 20px;
  line-height: 150%;
  color: #ffffff;
}

.lang-btn {
  background-color: hsla(0, 0%, 100%, 0.102);
  gap: 8px;
}

.header__register-btn {
  background-color: #06b48b;
}
/* BTN */
</style>
