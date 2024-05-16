<script setup lang="ts"></script>

<template>
  <section class="hero">
    <div class="container hero__container">
      <h1 class="hero__title">The Third International Pharmaceutical Forum of Uzbekistan</h1>
      <p class="hero__text">
        The largest international event dedicated to solving the most pressing problems of the pharmaceutical industry
        of the new Uzbekistan
      </p>
      <div class="hero__btn-wrapper">
        <div class="hero-btn">
          <img width="32" height="32" src="@/assets/images/clock.svg" alt="clock" />
          <span>May 30-31, 2024</span>
        </div>
        <a class="hero-btn" href="#">
          <img width="32" height="32" src="@/assets/images/location.svg" alt="clock" />
          <span>InterContinental Tashkent - Shakhrisabz Street 2</span>
        </a>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero {
  background-color: #044636;
  color: #fff;
}

.hero__container {
  display: flex;
  align-items: center;
  flex-direction: column;
  padding-top: 260px;
  padding-bottom: 280px;
}

.hero__title {
  font-size: 70px;
  font-weight: 700;
  line-height: 120%;
  text-align: center;
  margin-bottom: 12px;
  max-width: 1620px;
}

.hero__text {
  margin-bottom: 36px;
  max-width: 725px;
  font-size: 20px;
  font-weight: 400;
  line-height: 150%;
  text-align: center;
}

.hero__btn-wrapper {
  display: flex;
  align-items: center;
  gap: 16px;
}

.hero-btn {
  background-color: hsla(0, 0%, 100%, 0.102);
  border-radius: 20px;
  cursor: pointer;
  padding: 14px 24px;
  display: flex;
  align-items: center;
  font-size: 20px;
  font-weight: 500;
  gap: 8px;
  line-height: 150%;
}

/* MEDIA */
@media screen and (max-width: 991px) {
  .hero__title {
    font-size: 60px;
  }
  .hero__container {
    padding-top: 130px;
    padding-bottom: 130px;
  }
}

@media screen and (max-width: 768px) {
  .hero__container {
    padding-top: 60px;
    padding-bottom: 60px;
  }
  .hero__title {
    font-size: 32px;
  }
  .hero__btn-wrapper {
    flex-direction: row;
  }
  .hero-btn {
    font-size: 18px;
    padding: 8px 10px;
  }
}
@media screen and (max-width: 721px) {
  .hero__btn-wrapper {
    flex-direction: column;
  }
  .hero-btn {
    text-align: center;
  }
}
/* MEDIA */
</style>
