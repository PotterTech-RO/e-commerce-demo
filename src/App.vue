<template>
  <NavigationBar />
  <HomePage />
</template>

<script setup>
import HomePage from './pages/HomePage.vue';
import NavigationBar from './components/NavigationBar.vue'

</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  /* margin-top: 60px; */
  margin: 0;
  padding: 0;
}
</style>
