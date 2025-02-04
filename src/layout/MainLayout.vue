<template>
  <div style="position: fixed; z-index: -4; top: 0px; left: 0px; height: 100%; width: 100%">
    <div
      style="
        position: absolute;
        top: 0;
        z-index: -1;
        height: 150%;
        width: 100%;
        background: radial-gradient(
            ellipse 80% 80% at 50% -20%,
            rgba(120, 119, 198, 0.3),
            rgba(255, 255, 255, 0)
          ),
          #0a0a0a;
      "
    ></div>
  </div>
  <header>
    <MainHeader />
  </header>
  <main>
    <RouterView />
  </main>
  <footer>
    <MainFooter />
  </footer>
</template>

<script setup lang="ts">
import MainHeader from '@/components/MainHeader.vue'
import MainFooter from '@/components/MainFooter.vue';
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,200..1000;1,200..1000&display=swap');
body {
  font-family: 'Nunito', sans-serif;
}
</style>
