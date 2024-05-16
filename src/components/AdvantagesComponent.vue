<script setup lang="ts">
import { useImage } from '../composables/useImage'

const advantages = [
  {
    translateY: 'translateY(-85px)',
    img: 'advantages/adv1.svg',
    title: 'Topics',
    text: 'A rich business program, including unique thematic sessions, round tables, seminars and master classes',
  },
  {
    translateY: 'translateY(-90px)',
    img: 'advantages/adv2.svg',
    title: 'Experience',
    text: 'The event is intended to become a platform for the exchange of best practices between experts in the pharmaceutical market',
  },
  {
    translateY: 'translateY(-40px)',
    img: 'advantages/adv3.svg',
    title: 'Networking',
    text: 'Establishment of personal informal contacts with people of a narrow specialization with the least effort and time spent on business trips &nbsp;',
  },
  {
    translateY: 'translateY(-77px)',
    img: 'advantages/adv4.svg',
    title: 'Exclusivity',
    text: 'Industry-unique event',
  },
  {
    translateY: 'translateY(-43px)',
    img: 'advantages/adv5.svg',
    title: 'Partnership',
    text: 'Formation and expansion of the base of potential business partners',
  },
  {
    translateY: 'translateY(-50px)',
    img: 'advantages/adv6.svg',
    title: 'Trends',
    text: 'Discussion of the upcoming market trends',
  },
]
</script>

<template>
  <section class="advantages">
    <div class="container advatages__container">
      <h2 class="advantages__title">Advantages</h2>
      <div class="advantages-wrapper">
        <div class="advantages__bg">
          <img class="advantages__bg-img" src="@/assets/images/adv-bg.png" alt="adv bg" />
        </div>
        <ul class="advantages__list">
          <li v-for="advantage in advantages" :key="advantage.title" class="advantages__item-wrapper">
            <div class="advantages__item">
              <div :style="{ transform: advantage.translateY }" class="advantages__list-img-wrapper">
                <img class="advantages__list-img" :src="useImage(advantage.img)" :alt="advantage.title" />
              </div>
              <div class="advantages__content">
                <h3 class="advantages__list-title">{{ advantage.title }}</h3>
                <p class="advantages__list-text">{{ advantage.text }}</p>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
.advantages {
  padding: 160px 0;
}

.advantages__title {
  align-items: center;
  display: flex;
  justify-content: center;
  color: #1c2f3f;
  font-size: 48px;
  line-height: 150%;
  margin-bottom: 32px;
  width: 100%;
}

.advantages-wrapper {
  position: relative;
}

.advantages__bg {
  left: 0;
  position: absolute;
  top: 50px;
}

.advantages__bg-img {
  object-fit: cover;
  width: 100%;
  height: 100%;
  object-position: center;
}

.advantages__list {
  display: flex;
}

.advantages__item-wrapper {
  padding-left: 12px;
  padding-right: 12px;
  flex: 0 0 16.66666667%;
  max-width: 16.66666667%;
}

.advantages__item {
  height: 100%;
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
}

.advantages__content {
  border-radius: 20px;
  gap: 10px;
  height: calc(100% - 100px);
  padding: 20px;
  display: flex;
  width: 100%;
  flex-direction: column;
  align-items: flex-start;
  background-color: #e0f6f1;
  position: relative;
  z-index: 9;
}

.advantages__list-img-wrapper {
  padding-top: 120px;
  position: relative;
}

.advantages__list-img-wrapper::before {
  border-right: 2px dashed #059a77;
  bottom: 0;
  content: '';
  height: 100%;
  left: 50%;
  margin-left: -1px;
  position: absolute;
  transform: translateY(100%);
  width: 1px;
}

.advantages__list-img {
  width: 100px;
  height: 100px;
  display: flex;
}

.advantages__list-title {
  font-size: 28px;
  line-height: 150%;
  color: #1c2f3f;
  font-weight: 700;
}

.advantages__list-text {
  font-size: 18px;
  line-height: 140%;
  color: #1c2f3f;
  font-weight: 500;
}

@media screen and (max-width: 1200px) {
  .advantages__list {
    flex-wrap: wrap;
  }
  .advantages__item-wrapper {
    flex: 0 0 30%;
    max-width: 30%;
  }
}

@media only screen and (max-width: 991px) {
  .advantages {
    padding: 80px 0;
  }
}

@media screen and (max-width: 768px) {
  .advantages {
    padding: 40px 0;
  }
  .advantages__item-wrapper {
    flex: 0 0 50%;
    max-width: 50%;
  }
}

@media screen and (max-width: 576px) {
  .advantages__item-wrapper {
    flex: 0 0 100%;
    max-width: 100%;
  }
}
</style>
