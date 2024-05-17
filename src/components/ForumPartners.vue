<script setup lang="ts">
import { useImage } from '../composables/useImage'

const partners1 = [
  {
    img: 'partners/p1.png',
    link: '#',
  },
]

const partners2 = [
  {
    img: 'partners/p2.png',
    link: '#',
  },
  {
    img: 'partners/p3.jpg',
    link: '#',
  },
]

const partners3 = [
  {
    img: 'partners/p4.png',
    link: '#',
  },
  {
    img: 'partners/p5.png',
    link: '#',
  },
  {
    img: 'partners/p6.jpg',
    link: '#',
  },
  {
    img: 'partners/p7.png',
    link: '#',
  },
  {
    img: 'partners/p8.png',
    link: '#',
  },
  {
    img: 'partners/p9.png',
    link: '#',
  },
  {
    img: 'partners/p10.jpg',
    link: '#',
  },
]
</script>

<template>
  <section class="partner">
    <div class="partner__container container">
      <h2 class="partner__title">Forum Partners</h2>
      <div class="partner-group">
        <h3 class="partner-group__title">General Partner</h3>
        <ul class="partner-group__list">
          <li v-for="partner1 in partners1" :key="partner1.img" class="partner-group__item">
            <a class="partner-group__link" href="#">
              <div class="partner-group__img-wrapper">
                <img class="partner-group__img" :src="useImage(partner1.img)" :alt="partner1.img" />
              </div>
            </a>
          </li>
        </ul>
      </div>
      <div class="partner-group">
        <h3 class="partner-group__title">Main Partner</h3>
        <ul class="partner-group__list">
          <li v-for="partner2 in partners2" :key="partner2.img" class="partner-group__item">
            <a class="partner-group__link" href="#">
              <div class="partner-group__img-wrapper">
                <img class="partner-group__img" :src="useImage(partner2.img)" :alt="partner2.img" />
              </div>
            </a>
          </li>
        </ul>
      </div>
      <div class="partner-group">
        <h3 class="partner-group__title">Partner</h3>
        <ul class="partner-group__list">
          <li v-for="partner3 in partners3" :key="partner3.img" class="partner-group__item">
            <a class="partner-group__link" href="#">
              <div class="partner-group__img-wrapper">
                <img class="partner-group__img" :src="useImage(partner3.img)" :alt="partner3.img" />
              </div>
            </a>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<style scoped>
.partner {
  color: #1c2f3f;
  padding: 160px 0;
  font-weight: 700;
}

.partner__title {
  font-size: 48px;
  line-height: 150%;
  text-align: center;
  margin-bottom: 8px;
}

.partner-group__title {
  font-size: 28px;
  line-height: 130%;
  margin-bottom: 24px;
  margin-top: 24px;
  text-align: center;
}

.partner-group__list {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  row-gap: 24px;
}

.partner-group__item {
  flex: 0 0 16.66666667%;
  max-width: 16.66666667%;
  padding-left: 12px;
  padding-right: 12px;
}

.partner-group__link {
  border: 1px solid #c5d4e0;
  border-radius: 20px;
  height: 180px;
  padding: 20px;
  display: flex;
  align-items: center;
  justify-content: center;
}

.partner-group__img-wrapper {
  height: 100%;
  overflow: hidden;
  width: 100%;
  object-fit: contain;
}

.partner-group__img {
  object-fit: contain;
  height: 100%;
  object-position: center;
  width: 100%;
}

@media only screen and (max-width: 991px) {
  .partner {
    padding: 80px 0;
  }
  .partner-group__item {
    flex: 0 0 33.33333%;
    max-width: 33.33333%;
  }
}

@media only screen and (max-width: 768px) {
  .partner {
    padding: 40px 0;
  }
  .partner-group__item {
    flex: 0 0 50%;
    max-width: 50%;
  }
}
@media only screen and (max-width: 576px) {
  .partner-group__item {
    flex: 0 0 100%;
    max-width: 100%;
  }
}
</style>
