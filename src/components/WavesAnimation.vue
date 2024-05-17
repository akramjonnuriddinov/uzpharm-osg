<script setup lang="ts">
defineProps(['fill'])
</script>

<template>
  <section class="waves-wrapper">
    <svg
      class="waves"
      xmlns="http://www.w3.org/2000/svg"
      xmlns:xlink="http://www.w3.org/1999/xlink"
      viewBox="0 24 150 28"
      preserveAspectRatio="none"
      shape-rendering="auto"
    >
      <defs>
        <path id="gentle-wave" d="M-160 44c30 0 58-18 88-18s 58 18 88 18 58-18 88-18 58 18 88 18 v44h-352z"></path>
      </defs>
      <g class="parallax">
        <use xlink:href="#gentle-wave" x="48" y="0" fill="#C1EDE2"></use>
        <use xlink:href="#gentle-wave" x="48" y="3" :fill="fill"></use>
      </g>
    </svg>
  </section>
</template>

<style scoped>
.waves-wrapper {
  height: 70px;
  position: relative;
  background-color: #ffffff;
}

.waves {
  bottom: 0;
  height: 15vh;
  left: 0;
  max-height: 150px;
  min-height: 100px;
  position: absolute;
  width: 100%;
}

.parallax > use:first-child {
  animation-delay: -2s;
  animation-duration: 7s;
  animation: move 15s cubic-bezier(0.55, 0.5, 0.45, 0.5) infinite;
}

.parallax > use:nth-child(2) {
  animation-delay: -3s;
  animation-duration: 10s;
}

.parallax > use {
  animation: move 15s cubic-bezier(0.55, 0.5, 0.45, 0.5) infinite;
}

@keyframes move {
  0% {
    transform: translate3d(-90px, 0, 0);
  }
  100% {
    transform: translate3d(85px, 0, 0);
  }
}
</style>
