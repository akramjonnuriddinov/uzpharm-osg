<script setup lang="ts">
import { useImage } from '../composables/useImage'
import WavesAnimation from '@/components/WavesAnimation.vue'

const participants = [
  {
    link: '#',
    img: 'part/gerb.png',
    title: 'Ministry of Investment, Industry and Trade of the Republic of Uzbekistan',
  },
  {
    link: '#',
    img: 'part/agency.png',
    title: 'The Pharmaceutical Industry Development Agency under the Ministry of Health of the Republic of Uzbekistan.',
  },
  {
    link: '#',
    img: 'part/agency.png',
    title:
      'Agency for the Development of the Pharmaceutical industry under the Ministry of Health of the Republic of Uzbekistan',
  },
]
</script>

<template>
  <waves-animation fill="#E0F6F1" />
  <section class="part">
    <div class="container part__container">
      <h2 class="part__title">Organizers of the Forum</h2>

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
  padding: 160px 0;
  background-color: #e0f6f1;
}

.part__title {
  font-size: 48px;
  line-height: 150%;
  color: #1c2f3f;
  font-weight: 700;
  margin-bottom: 0.5em;
  text-align: center;
}

.part__list {
  display: flex;
  flex-wrap: wrap;
}

.part__list-item {
  width: 100%;
  max-width: calc(100% / 3);
  padding: 12px;
  display: flex;
}

.part__list-link {
  display: flex;
  flex-direction: column;
  align-items: center;
  text-align: center;
  gap: 20px;
  background-color: #fff;
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
  .part__list-item {
    max-width: 50%;
  }
}

@media screen and (max-width: 768px) {
  .part {
    padding: 40px 0;
  }
  .part__list-item {
    max-width: 100%;
  }
}
</style>
