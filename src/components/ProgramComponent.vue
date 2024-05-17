<script setup lang="ts">
import WavesAnimation from '@/components/WavesAnimation.vue'
</script>

<template>
  <waves-animation fill="#059A77" />
  <section class="program">
    <div class="container program__container">
      <h2 class="program__title">Program</h2>
      <p class="program__text">The final version of the forum program will be available soon</p>
      <div class="program__btn-wrapper">
        <div class="program__border"></div>
        <button class="program__btn program__btn--active">DAY 1</button>
        <button class="program__btn program__btn--active">DAY 2</button>
        <div class="program__border"></div>
      </div>
      <div class="program-inner">
        <ul class="program__list">
          <li class="program__item">
            <span class="program__list-time"></span>
            <span class="program__list-text">MAIN HALL</span>
          </li>
          <li v-for="i in 10" :key="i" class="program__item">
            <span class="program__list-time">08.30 – 09.45</span>
            <span class="program__list-text">Registration</span>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
.program {
  background-color: #059a77;
  color: #fff;
  padding: 160px 0;
  overflow-x: hidden;
  position: relative;
}

.program::before {
  background-image: url('@/assets/images/hero-bg.png');
  background-repeat: no-repeat;
  background-size: 100%;
  content: '';
  height: 500px;
  opacity: 0.1;
  position: absolute;
  top: 50%;
  width: 500px;
  z-index: 1;
  animation: rotate360 60s linear infinite;
  left: 0;
  transform: translate(-25%, -50%) rotate(90deg);
}

.program::after {
  background-image: url('@/assets/images/hero-bg.png');
  background-repeat: no-repeat;
  background-size: 100%;
  content: '';
  height: 500px;
  opacity: 0.1;
  position: absolute;
  top: 50%;
  width: 500px;
  z-index: 1;
  animation: rotate360right 60s linear infinite;
  right: 0;
  transform: translate(25%, -50%);
}

@keyframes rotate360 {
  0% {
    transform: translate(-25%, -50%) rotate(0);
  }
  100% {
    transform: translate(-25%, -50%) rotate(1turn);
  }
}

@keyframes rotate360right {
  0% {
    transform: translate(25%, -50%) rotate(90deg);
  }
  100% {
    transform: translate(25%, -50%) rotate(1turn);
  }
}

.program__title {
  font-size: 48px;
  font-weight: 700;
  margin-bottom: 0.5em;
  line-height: 150%;
  text-align: center;
}

.program__text {
  font-size: 20px;
  font-weight: 400;
  line-height: 150%;
  opacity: 0.8;
  text-align: center;
}

.program__btn-wrapper {
  display: flex;
  align-items: center;
  gap: 8px;
}

.program__border {
  border-top: 1px dashed hsla(0, 0%, 100%, 0.4);
  flex-grow: 1;
  height: 1px;
}

.program__btn {
  background-color: transparent;
  border: 1px solid hsla(0, 0%, 100%, 0.4);
  border-radius: 20px;
  cursor: pointer;
  outline: none;
  font-weight: 600;
  padding: 14px 24px;
  font-size: 20px;
  gap: 8px;
  line-height: 150%;
  color: #fff;
}

.program-inner {
  display: flex;
  flex-direction: column;
  margin-left: auto;
  margin-right: auto;
  flex: 0 0 66.66666667%;
  max-width: 66.66666667%;
}

.program__list {
  display: flex;
  flex-direction: column;
  row-gap: 16px;
}

.program__item {
  display: flex;
}

.program__list-time {
  font-size: 22px;
  line-height: 150%;
  padding-left: 12px;
  padding-right: 12px;
  display: block;
  max-width: 160px;
  width: 100%;
}

.program__list-text {
  font-size: 22px;
  line-height: 150%;
  font-weight: 700;
  margin-bottom: 0.5em;
  padding-left: 12px;
  padding-right: 12px;
}

@media only screen and (max-width: 1200px) {
  .program:after,
  .program:before {
    content: '';
    height: 350px;
    width: 350px;
  }
}

@media only screen and (max-width: 991px) {
  .prgoram {
    padding: 80px 0;
  }
  .program:after,
  .program:before {
    content: '';
    height: 250px;
    width: 250px;
  }
}

@media screen and (max-width: 768px) {
  .prgoram {
    padding: 40px 0;
  }
  .program-inner {
    flex: 0 0 100%;
    max-width: 100%;
  }
  .program__item {
    flex-direction: column;
  }
  .program:before {
    top: 25%;
  }
  .program:after {
    top: 75%;
  }
}
</style>
