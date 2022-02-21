<script setup>
import { RouterLink, RouterView } from "vue-router";
</script>

<template>
  <header>
    <img alt="Vue logo" class="logo" src="@/assets/logo.svg" width="125" height="125" />

    <div class="wrapper">
      <h1>Welcome, Riley</h1>

      <nav>
        <RouterLink to="/">Home</RouterLink>
        <!-- <RouterLink to="/about">About</RouterLink> -->
      </nav>
    </div>
  </header>

  <RouterView />
</template>

<style>
@import "@/assets/base.css";
#app {
  display: flex;
  justify-content: space-around;
  align-items: center;
  min-height: 100vh;
}
main {
  width: 50%;
}
header {
  width: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}
a {
  text-decoration: none;
  color: #e8c457;
  transition: 0.4s;
  padding: 10px;
}
img {
  margin: 10px;
}

@media (max-width: 1024px) {
  #app {
    flex-direction: column;
    min-height: 0;
  }
  header {
    width: 100%;
  }
}
</style>
