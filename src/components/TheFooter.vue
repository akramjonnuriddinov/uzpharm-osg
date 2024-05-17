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
      <div class="footer__item">
        <div class="phone-number">
          <div class="phone-number__top">
            <img class="phone-number__icon" src="@/assets/images/phone.svg" alt="phone" />
            <span>Phone number: </span>
          </div>
          <a class="phone-number__link" href="tel:+998991178899">+998 99 117 88 99</a>
        </div>
        <div class="phone-number">
          <div class="phone-number__top">
            <img class="phone-number__icon" src="@/assets/images/dot.svg" alt="phone" />
            <span>Address: </span>
          </div>
          <a class="phone-number__link" href="#">OOO “World Pharma Forum” Tashkent, 95A Amir Temur Avenue</a>
        </div>
      </div>
      <div class="footer__item">
        <div class="phone-number footer__links">
          <a class="phone-number__link" href="#">Program</a>
          <a class="phone-number__link" href="#">Participants </a>
          <a class="phone-number__link" href="#">Media</a>
        </div>
      </div>
      <div class="footer__item footer__item--signup">
        <div class="phone-number">
          <div class="phone-number__top">
            <img class="phone-number__icon" src="@/assets/images/phone.svg" alt="phone" />
            <span>May 30-31, 2024 </span>
          </div>
        </div>
        <div class="phone-number">
          <div class="phone-number__top">
            <img class="phone-number__icon" src="@/assets/images/dot.svg" alt="phone" />
            <span>InterContinental Tashkent - Shakhrisabz Street 2 </span>
          </div>
        </div>
        <button class="footer__register-btn">
          <span>Register</span>
          <img class="footer__register-btn-icon" src="@/assets/images/arrow-right-white.svg" alt="" />
        </button>
      </div>
    </div>
  </footer>
</template>

<style scoped>
.phone-number {
  display: flex;
  flex-direction: column;
  margin-bottom: 24px;
}

.phone-number__icon {
  width: 18px;
  height: 18px;
}

.phone-number__top {
  display: flex;
  align-items: center;
  gap: 8px;
  margin-bottom: 8px;
  font-weight: 600;
  font-size: 18px;
}

.phone-number__link {
  font-size: 20px;
  font-weight: 600;
  line-height: 150%;
}

.footer__links {
  gap: 16px;
}

.footer__item--signup {
  background-color: #06b48b;
  border-radius: 20px;
  display: flex;
  flex-direction: column;
  height: 100%;
  padding: 20px 26px;
  width: 100%;
}

.footer__register-btn {
  background-color: transparent;
  border: none;
  outline: none;
  display: flex;
  align-items: center;
  color: #fff;
  gap: 8px;
  font-size: 18px;
  font-weight: 400;
  line-height: 27px;
  font-weight: bold;
}

.footer__register-btn-icon {
  display: flex;
  width: 18px;
  height: 18px;
}
/*  */
.footer {
  background-color: #078b6c;
  padding: 60px 0;
  color: #fff;
}

.footer__container {
  display: flex;
  justify-content: space-between;
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
