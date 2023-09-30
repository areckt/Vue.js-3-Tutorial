<script setup>
import { RouterLink, RouterView } from 'vue-router'
import HelloWorld from './components/HelloWorld.vue'
</script>

<template>
  <header>
    <HelloWorld msg="Hello World" />
    <nav>
      <RouterLink to="/">Home</RouterLink>
      <RouterLink to="/about">About</RouterLink>
      <RouterLink to="/cards">Cards</RouterLink>
    </nav>
  </header>
  <RouterView />
</template>

<style scoped>
header {
  margin-bottom: 2rem;
}
nav {
  display: flex;
  gap: 1rem;
}
</style>
