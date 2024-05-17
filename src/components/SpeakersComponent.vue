<script setup lang="ts">
import { useImage } from '../composables/useImage'
import WavesAnimation from '@/components/WavesAnimation.vue'

const speakers = [
  {
    img: 'speakers/speaker1.png',
    name: 'Asilbek Khudayarov',
    position: 'Minister',
    description: 'Ministry of Health of the Republic of Uzbekistan',
  },
  {
    img: 'speakers/speaker2.png',
    name: 'Khurram Teshabayev',
    position: 'Deputy Minister',
    description: 'Ministry of Investments, Industry and Trade of the Republic of Uzbekistan',
  },
  {
    img: 'speakers/speaker3.png',
    name: 'Otabek Rustamovich Fozilkarimov',
    position: 'Deputy Minister',
    description: 'The Ministry of Economy and Finance of the Republic of Uzbekistan',
  },
  {
    img: 'speakers/speaker4.png',
    name: 'Abdulla Azizov',
    position: 'Director',
    description: 'The Pharmaceutical Industry Development Agency',
  },
  {
    img: 'speakers/speaker5.png',
    name: 'Abdiev Jahongir Ibragimovich',
    position: 'Chairman',
    description: 'The State Tax Committee of the Republic of Uzbekistan',
  },
  {
    img: 'speakers/speaker6.png',
    name: 'Agzam Nartaev',
    position: 'Head of Department',
    description: 'Regulation of the pharmaceutical sector and determination of the needs for medicinal products',
  },
  {
    img: 'speakers/speaker7.png',
    name: 'Alisher Smatillaevich Temirov',
    position: 'Director',
    description: 'Center for Pharmaceutical Product Safety',
  },
  {
    img: 'speakers/speaker8.png',
    name: 'Vyacheslav Lokshin',
    position: 'President',
    description: 'Association of International Pharmaceutical Manufacturers in the Republic of Kazakhstan',
  },
]
</script>

<template>
  <waves-animation fill="#E0F6F1" />
  <section class="speakers">
    <div class="container speakers__container">
      <div class="speakers__top">
        <h2 class="speakers__title">Main speakers</h2>
        <router-link class="see-all" to="/">
          <span>See all</span>
          <img class="see-all__img" src="@/assets/images/arrow-right.svg" alt="arrow right" />
        </router-link>
      </div>
    </div>
    <ul class="speakers__list">
      <li v-for="speaker in speakers" :key="speaker.name" class="speakers__list-item">
        <div class="speakers__list-inner">
          <img class="speakers__list-img" :src="useImage(speaker.img)" :alt="speaker.name" />
          <div class="speakers__list-content">
            <h3 class="speakers__list-title">{{ speaker.name }}</h3>
            <p class="speakers__list-text">{{ speaker.position }}</p>
            <p class="speakers__list-desc">{{ speaker.description }}</p>
          </div>
        </div>
      </li>
    </ul>
  </section>
</template>

<style scoped>
.speakers {
  background-color: #e0f6f1;
  padding: 200px 0;
}

.speakers__top {
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  margin-bottom: 32px;
}

.speakers__title {
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

.speakers__list {
  display: flex;
  justify-content: space-between;
  row-gap: 24px;
  flex-wrap: wrap;
}

.speakers__list-item {
  display: block;
  max-width: 25%;
  padding-left: 12px;
  padding-right: 12px;
}

.speakers__list-inner {
  display: flex;
  flex-direction: column;
  height: 100%;
}

.speakers__list-img {
  border-radius: 20px;
  flex: 350px 0 0;
  height: 350px;
  overflow: hidden;
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}

.speakers__list-content {
  background-color: #fff;
  border-radius: 20px;
  display: flex;
  flex: 100% 1 1;
  flex-direction: column;
  padding: 16px;
}

.speakers__list-title {
  font-size: 20px;
  font-weight: 600;
  line-height: 150%;
  color: #1c2f3f;
  margin-bottom: 12px;
}

.speakers__list-text {
  color: #06b48b;
  font-size: 18px;
  font-weight: 600;
  line-height: 150%;
  margin-bottom: 16px;
}

.speakers__list-desc {
  border-top: 1px solid #c5d4e0;
  height: 100px;
  margin-bottom: 16px;
  margin-top: auto;
  padding-top: 16px;
  width: 100%;
  display: -webkit-box;
  overflow: hidden;
  text-overflow: ellipsis;
  -webkit-box-orient: vertical;
  -webkit-line-clamp: 3;
  font-size: 18px;
  font-weight: 600;
  line-height: 150%;
  opacity: 0.8;
}

/* MEDIA */
@media screen and (max-width: 1200px) {
  .speakers__list-item {
    max-width: 50%;
  }
}

@media only screen and (max-width: 991px) {
  .speakers {
    padding: 80px 0;
  }
}

@media screen and (max-width: 768px) {
  .speakers {
    padding: 40px 0;
  }
  .speakers__top {
    flex-direction: column;
  }
  .speakers__list-item {
    max-width: 100%;
  }
}
</style>
