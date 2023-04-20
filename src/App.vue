<script setup>
import WeddingTitle from './components/title.vue';
const imgUrl = new URL('assets/ring.jpg', import.meta.url).href;
</script>

<template>
  <div class="content">
    <wedding-title />
    <p>Save the date coming soon!</p>
  </div>
  <div class="background" :style="`background-image: url(${imgUrl});`"></div>
</template>

<style scoped lang="scss">
.background {
  height: 100vh;
  width: 100vw;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 10;
  background-position: center;
  background-size: cover;
  background-repeat: no-repeat;
}

.content {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  min-height: 100vh;
  width: 100vw;
  position: fixed;
  top: 0;
  left: 0;
  z-index: 20;
  backdrop-filter: blur(3px);
  transition: backdrop-filter 0.3s ease-in-out;
  background-color: rgba(var(--background), 0.6);

  p {
    font-family: WeddingSubtitle;
    font-weight: bolder;
    font-size: 24px;
    margin: 0px;
    padding: 0px;
    color: rgb(var(--text));
  }
}
</style>
