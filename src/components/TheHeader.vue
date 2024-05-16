<script setup lang="ts">
import MobileHeader from '@/components/MobileHeader.vue'
import { ref } from 'vue'
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

const isShow = ref(false)
</script>

<template>
  <mobile-header
    @close-mobile-navbar="isShow = false"
    class="mobile-header"
    :class="{ 'translate-x-full': !isShow, 'translate-x-none': isShow }"
  />
  <header class="header" :style="{ display: isShow ? 'none' : 'flex' }">
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
      <button @click="isShow = true" class="hamburger-btn">
        <img class="hamburger-btn__img" src="@/assets/images/hamburger.svg" alt="hamburger btn" />
      </button>
    </div>
  </header>
</template>

<style scoped>
.translate-x-full {
  transform: translateX(-100%);
}

.translate-x-none {
  transform: translateX(0);
}

.mobile-header {
  display: none;
}

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
  position: relative;
  z-index: 1;
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

.navbar {
  display: flex;
}

.navbar__list {
  display: flex;
  align-items: center;
  gap: 40px;
  font-weight: 600;
}

.navbar__item {
  font-size: 20px;
  line-height: 150%;
  transition: all 0.2s ease;
  font-weight: 500;
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

.hamburger-btn {
  display: none;
  background-color: transparent;
  color: #fff;
  border: none;
}

/* MEDIA */
@media screen and (max-width: 1200px) {
  .mobile-header {
    display: flex;
  }
  .hamburger-btn {
    display: flex;
  }
  .navbar {
    display: none;
  }
  .header__btn-wrapper {
    display: none;
  }
}
/* /MEDIA */
</style>
