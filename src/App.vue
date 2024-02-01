<script setup>
import HelloWorld from './components/HelloWorld.vue'
import SearchList from './components/SearchList.vue'
import Header from './components/Header.vue'
import LandingPage from './views/LandingPage.vue'
</script>

<template>
  <LandingPage/>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
