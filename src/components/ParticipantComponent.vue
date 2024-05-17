<script setup lang="ts">
import { useImage } from '../composables/useImage'

const participants = [
  {
    link: '#',
    img: 'part/gerb.png',
    title: 'Ministry of Investment, Industry and Trade of the Republic of Uzbekistan',
  },
  {
    link: '#',
    img: 'part/gerb.png',
    title: 'Ministry of Health of the Republic of Uzbekistan',
  },
  {
    link: '#',
    img: 'part/agency.png',
    title:
      'Agency for the Development of the Pharmaceutical industry under the Ministry of Health of the Republic of Uzbekistan',
  },
  {
    link: '#',
    img: 'part/soliq.png',
    title: 'State Tax Committee',
  },
  {
    link: '#',
    img: 'part/custom.png',
    title: 'State Customs Committee',
  },
  {
    link: '#',
    img: 'part/acru.png',
    title: 'Antimonopoly Committee of Uzbekistan',
  },
  {
    link: '#',
    img: 'part/gerb.png',
    title: 'Agency for Intellectual Property of the Republic of Uzbekistan',
  },
]
</script>

<template>
  <section class="part">
    <div class="container part__container">
      <div class="part__top">
        <h2 class="part__title">Participants</h2>
        <router-link class="see-all" to="/">
          <span>See all</span>
          <img class="see-all__img" src="@/assets/images/arrow-right.svg" alt="arrow right" />
        </router-link>
      </div>
      <ul class="part__list">
        <li v-for="participant in participants" :key="participant.title" class="part__list-item">
          <a class="part__list-link" :href="participant.link">
            <img class="part__list-img" :src="useImage(participant.img)" :alt="participant.title" />
            <h3 class="part__list-title">{{ participant.title }}</h3>
          </a>
        </li>
      </ul>
    </div>
  </section>
</template>

<style scoped>
.part {
  padding: 280px 0 160px;
}

.part__top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  margin-bottom: 32px;
}

.part__title {
  font-size: 48px;
  line-height: 150%;
  color: #1c2f3f;
  font-weight: 700;
  margin-bottom: 0.5em;
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

.see-all__img {
  width: 16px;
  height: 16px;
}

.part__list {
  display: flex;
  flex-wrap: wrap;
}

.part__list-item {
  width: 100%;
  max-width: 25%;
  padding: 12px;
}

.part__list-link {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 20px;
  background-color: #ebf2f0;
  border-radius: 20px;
  color: #1c2f3f;
  padding: 24px;
  height: 100%;
  font-size: 20px;
  font-weight: 600;
  line-height: 150%;
}

@media screen and (max-width: 1200px) {
  .part__list-item {
    max-width: 50%;
  }
}

@media only screen and (max-width: 991px) {
  .part {
    padding: 80px 0;
  }
}

@media screen and (max-width: 768px) {
  .part {
    padding: 40px 0;
  }
  .part__list-item {
    max-width: 100%;
  }
  .part__top {
    flex-direction: column;
  }
}
</style>
