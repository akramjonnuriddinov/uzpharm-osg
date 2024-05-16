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
  <header class="mobile-header">
    <div class="container mobile-header__container">
      <div class="mobile-header__top">
        <router-link class="mobile-header__logo" to="/">
          <img class="mobile-header__logo-img" src="@/assets/images/logo.svg" alt="site logo" />
          <span
            >Third International Pharmaceutical
            <br />
            Forum of Uzbekistan
          </span>
        </router-link>
        <button @click="$emit('close-mobile-navbar')" class="close-mobile-navbar">
          <img class="close-mobile-navbar__img" src="@/assets/images/close.svg" alt="hamburger btn" />
        </button>
      </div>
      <nav class="navbar">
        <ul class="navbar__list">
          <li v-for="link in links" :key="link.path" class="navbar__item">
            <router-link :to="link.path">{{ link.name }}</router-link>
          </li>
        </ul>
      </nav>
      <div class="mobile-header__btn-wrapper">
        <button class="main-btn lang-btn">
          <span>RUS</span>
        </button>
        <button class="main-btn lang-btn">
          <span>EN</span>
        </button>
        <a class="main-btn mobile-header__register-btn" href="#">Register</a>
      </div>
    </div>
  </header>
</template>

<style scoped>
.mobile-header {
  position: absolute;
  top: 0;
  z-index: 999;
  width: 100%;
  padding-bottom: 30px;
  transition: transform 0.3s ease;
  background-color: #044636;
  color: #ffffff;
  min-height: 100vh;
  bottom: 0;
}

.mobile-header__container {
  display: flex;
  flex-direction: column;
}

.mobile-header__top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  border-bottom: 1px solid #f0f0f0;
  padding-bottom: 24px;
  padding-top: 24px;
  position: sticky;
  top: 0;
  background-color: #044636;
}

.mobile-header__logo {
  display: flex;
  align-items: center;
  font-size: 19px;
  font-weight: 500;
  line-height: 140%;
}

.mobile-header__logo-img {
  width: 60px;
  height: 60px;
  display: flex;
  margin-right: 8px;
}

.navbar {
  padding-top: 24px;
}

.navbar__list {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
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
.mobile-header__btn-wrapper {
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

.mobile-header__register-btn {
  background-color: #06b48b;
}
/* BTN */

.close-mobile-navbar {
  background-color: transparent;
  color: #fff;
  border: none;
}

/* MEDIA */
@media screen and (max-width: 1200px) {
}
/* /MEDIA */
</style>
