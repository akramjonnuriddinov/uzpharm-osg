<script setup lang="ts">
import { ref, onMounted } from 'vue'
import TheHeader from '@/components/TheHeader.vue'
import HeroComponent from '@/components/HeroComponent.vue'
import InternationForum from '@/components/InternationForum.vue'
import ParticipantComponent from '@/components/ParticipantComponent.vue'
import SpeakersComponent from '@/components/SpeakersComponent.vue'
import AdvantagesComponent from '@/components/AdvantagesComponent.vue'
import AppLoader from '@/components/AppLoader.vue'
import ProgramComponent from '@/components/ProgramComponent.vue'
import ForumPartners from '@/components/ForumPartners.vue'
import OrganizerForum from '@/components/OrganizerForum.vue'
import CostComponent from '@/components/CostComponent.vue'

const isLoading = ref(true)

onMounted(() => {
  if (isLoading.value) document.body.style.overflow = 'hidden'
})

setTimeout(() => {
  isLoading.value = false
  document.body.style.overflow = 'auto'
}, 1500)
</script>

<template>
  <app-loader v-if="isLoading" />
  <div class="home">
    <the-header />
    <hero-component />
    <internation-forum />
    <participant-component />
    <speakers-component />
    <advantages-component />
    <program-component />
    <forum-partners />
    <organizer-forum />
    <cost-component />
  </div>
</template>

<style scoped>
.home {
  overflow-x: hidden;
}
</style>
