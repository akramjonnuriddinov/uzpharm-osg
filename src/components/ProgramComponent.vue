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
      <h3>Main Hall</h3>
      <ul class="program__list">
        <li class="program__item">
          <span>08.30 – 09.45</span>
          <span>Registration</span>
        </li>
      </ul>
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
</style>
