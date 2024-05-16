<script setup lang="ts">
import TheHeader from '@/components/TheHeader.vue'
import HeroComponent from '@/components/HeroComponent.vue'
import InternationForum from '@/components/InternationForum.vue'
import ParticipantComponent from '@/components/ParticipantComponent.vue'
import SpeakersComponent from '@/components/SpeakersComponent.vue'
</script>

<template>
  <div class="home">
    <the-header />
    <hero-component />
    <internation-forum />
    <participant-component />
    <speakers-component />
  </div>
</template>

<style scoped>
.home {
  overflow-x: hidden;
}
</style>
