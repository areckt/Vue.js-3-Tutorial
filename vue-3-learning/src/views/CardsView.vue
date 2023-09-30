<script setup>
import TheCard from '../components/TheCard.vue'
</script>

<template>
  <div class="cards-wrapper">
    <TheCard :num="1"/>
    <TheCard :num="2"/>
    <TheCard :num="3"/>
    <TheCard :num="4"/>
  </div>
</template>

<style scoped>
.cards-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 1rem;
}
</style>