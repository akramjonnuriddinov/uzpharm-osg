<script setup lang="ts">
import TheHeader from '@/components/TheHeader.vue'
import HeroComponent from '@/components/HeroComponent.vue'
import InternationForum from '@/components/InternationForum.vue'
</script>

<template>
  <div class="home">
    <the-header />
    <hero-component />
    <internation-forum />
  </div>
</template>

<style scoped>
.home {
  overflow-x: hidden;
}
</style>
