<script setup>
import Weather from "../components/Weather.vue";
</script>

<template>
  <main>
    <!-- <TheWelcome /> -->
    <h2>Quick Links</h2>
    <ul>
      <a href="">Email</a>
      <a href="">Canvas</a>
      <a href="">Skyward</a>
    </ul>
    <h2>Weather</h2>
    <Weather></Weather>
  </main>
</template>

<style scoped>
ul {
  display: flex;
  flex-direction: column;
}
</style>
