<script setup lang="ts">
import WavesAnimation from '@/components/WavesAnimation.vue'
</script>

<template>
  <waves-animation fill="#078b6c" />
  <footer class="footer">
    <div class="container footer__container">
      <div class="footer__item">
        <router-link class="footer__logo" to="/">
          <img class="footer__logo-img" src="/src/assets/images/footer-logo.svg" alt="footer logo" />
          <span>
            Third International Pharmaceutical <br />
            Forum of Uzbekistan
          </span>
        </router-link>
        <span class="privacy">
          © 2024 International <br />
          Pharmceutical Forum of Uzbekistan
        </span>
        <div class="osg osg-footer-top">
          <span class="osg__top">Website development:</span>
          <a>Online Service Group</a>
        </div>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  background-color: #078b6c;
  padding: 60px 0;
  color: #fff;
}

.footer__item {
  display: block;
  flex: 0 0 25%;
  max-width: 25%;
}

.footer__logo {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 19px;
  font-weight: 500;
  line-height: 140%;
}

.footer__logo-img {
  display: flex;
  width: 60px;
  height: 60px;
}

.privacy {
  font-size: 18px;
  line-height: 150%;
  opacity: 0.8;
  margin-bottom: 24px;
  font-weight: 600;
  display: flex;
}

.osg__top {
  font-size: 18px;
  line-height: 150%;
  opacity: 0.8;
  font-weight: 600;
}

.osg a {
  font-weight: 600;
  font-size: 18px;
  line-height: 150%;
  margin-left: 4px;
}
</style>
