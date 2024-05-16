<script setup lang="ts">
const forums = [
  {
    title: '2 days',
    text: 'BUSINESS COMMUNICATION AND NETWORKING',
  },
  {
    title: '8+',
    text: 'THEMATIC SESSIONS + ROUND TABLES + WORKSHOPS',
  },
  {
    title: '250+',
    text: 'PARTICIPANTS',
  },
]
</script>

<template>
  <section class="forum">
    <div class="container forum__container">
      <div class="forum__img-wrapper forum__img-wrapper-first">
        <img class="forum__img" src="@/assets/images/forum1.png" alt="forum" />
      </div>
      <div class="forum__content">
        <h2 class="forum__title">International Pharmaceutical Forum of Uzbekistan</h2>
        <p class="forum__text">
          The First International Pharmaceutical Forum of Uzbekistan declared itself to be a unique professional
          international platform for the leaders of the pharmaceutical industry, with the participation of the heads of
          the largest manufacturers, distributors, regulators, licensors of production technologies, lawyers and
          consulting specialists working in this field and many others.
        </p>
      </div>
      <div class="forum__img-wrapper">
        <img class="forum__img" src="@/assets/images/forum2.png" alt="forum 2" />
      </div>
    </div>
    <div class="container forum__count">
      <ul class="forum__list">
        <li v-for="forum in forums" :key="forum.title" class="forum__item">
          <div class="forum__content-wrapper">
            <h4 class="forum__list-title">{{ forum.title }}</h4>
            <p class="forum__list-text">{{ forum.text }}</p>
          </div>
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.forum {
  background-color: #044636;
  color: #ffffff;
}

.forum__container {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-bottom: 80px;
}

.forum__content {
  display: flex;
  flex-direction: column;
  text-align: center;
  padding-left: 12px;
  padding-right: 12px;
}

.forum__title {
  font-size: 40px;
  line-height: 140%;
  font-weight: 500;
  margin-bottom: 0.5em;
}

.forum__text {
  font-size: 20px;
  line-height: 150%;
  opacity: 0.8;
}

.forum__img-wrapper {
  display: flex;
  border-radius: 16px;
  overflow: hidden;
  max-width: 25%;
  width: 100%;
  height: 278px;
  padding-right: 12px;
  padding-left: 12px;
}

.forum__img {
  width: 100%;
  object-fit: cover;
  height: 100%;
  border-radius: 16px;
}

/* FORUM COUNT */
.forum__list {
  display: flex;
  transform: translateY(50%);
}

.forum__item {
  padding-left: 16px;
  padding-right: 16px;
  max-width: 1/3;
  width: 100%;
}

.forum__content-wrapper {
  display: flex;
  flex-direction: column;
  width: 100%;
  align-items: center;
  background-color: #06b48b;
  border-radius: 20px;
  height: 230px;
  justify-content: center;
  overflow: hidden;
  padding: 34px 40px;
  position: relative;
}

.forum__content-wrapper::after {
  background-image: url('@/assets/images/hero-bg.png');
  background-repeat: no-repeat;
  background-size: 100%;
  content: '';
  height: 140px;
  opacity: 0.1;
  position: absolute;
  right: 5px;
  top: 50%;
  transform: translate(25%, -50%) rotate(135deg);
  width: 140px;
}

.forum__list-title {
  font-size: 56px;
  font-weight: 500;
  line-height: 140%;
  text-align: center;
}

.forum__list-text {
  font-size: 24px;
  font-weight: 400;
  line-height: 150%;
  text-align: center;
}
/* /FORUM COUNT */

@media screen and (max-width: 1200px) {
  .forum__container {
    flex-direction: column;
    flex-flow: row wrap;
    row-gap: 24px;
  }
  .forum__content {
    order: -1;
  }
  .forum__img-wrapper {
    max-width: 50%;
  }
  .forum__list {
    flex-wrap: wrap;
    row-gap: 32px;
  }
  .forum__item {
    max-width: 50%;
  }
}

@media screen and (max-width: 991px) {
  .forum__list {
    transform: translateY(0);
    padding-bottom: 24px;
  }
}

@media screen and (max-width: 768px) {
  .forum__container {
    flex-direction: column;
    flex-flow: column;
    row-gap: 24px;
  }
  .forum__content {
    order: -1;
  }
  .forum__img-wrapper-first {
    order: -2;
  }
  .forum__img-wrapper {
    max-width: 100%;
  }
  .forum__item {
    max-width: 100%;
  }
}
</style>
