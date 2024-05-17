<script setup lang="ts"></script>

<template>
  <section class="cost">
    <div class="container cost__container">
      <h2 class="cost__title">Cost and conditions of participation</h2>

      <div>
        <div class="tab-btn-wrapper">
          <button class="main-btn tab-btn__first">Participation</button>
          <button class="see-all">Become a partner</button>
        </div>
        <div class="cost-card">
          <h3 class="cost-card__title">Cost</h3>
          <div class="cost-card__inner">
            <span class="cost-card__price">$1 500</span>
            <p class="cost-card__text">For one delegate</p>
            <button class="see-all cost-card__btn">Register</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.cost {
  padding: 160px 0;
}

.cost-card {
  max-width: 410px;
  width: 100%;
  border-radius: 20px;
  margin-left: auto;
  margin-right: auto;
  color: #fff;
}

.cost__title {
  font-family: Gilroy-Bold, sans-serif;
  font-size: 48px;
  line-height: 150%;
  color: #1c2f3f;
  margin-bottom: 40px;
  text-align: center;
}

.cost-card__title {
  background-color: #0ac398;
  display: flex;
  justify-content: center;
  padding: 15px 0;
  text-align: center;
  border-top-left-radius: 20px;
  border-top-right-radius: 20px;
}

.cost-card__inner {
  background-color: #07a781;
  padding: 32px 0;
  display: flex;
  flex-direction: column;
  align-items: center;
  border-bottom-left-radius: 20px;
  border-bottom-right-radius: 20px;
  position: relative;
}

.cost-card__inner::after {
  background-image: url('@/assets/images/hero-bg.png');
  background-repeat: no-repeat;
  background-size: 100%;
  content: '';
  height: 140px;
  left: 50%;
  opacity: 0.1;
  position: absolute;
  top: 20px;
  transform: translateX(-50%) rotate(135deg);
  width: 140px;
}

.cost-card__price {
  font-size: 40px;
  line-height: 130%;
  font-weight: 700;
  margin-bottom: 8px;
}

.cost-card__text {
  font-size: 24px;
  line-height: 130%;
  margin-bottom: 24px;
  font-weight: 600;
}

/* BTN */
.tab-btn-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 16px;
  margin-bottom: 32px;
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

.see-all {
  display: flex;
  align-items: center;
  gap: 8px;
  border-radius: 20px;
  cursor: pointer;
  outline: none;
  padding: 14px 24px;
  background-color: transparent;
  border: 1px solid rgba(28, 47, 63, 0.2);
  font-size: 20px;
  line-height: 150%;
}

.tab-btn__first {
  background-color: #06b48b;
}
/* BTN */

.cost-card__btn {
  background-color: #06b48b;
  color: #fff;
  margin-top: 24px;
  border: none;
}
</style>
