<script setup>
import ButtonPrimary from '../components/ButtonPrimary.vue'
defineProps({
  num: {
    type: Number,
    required: true
  }
})
</script>

<template>
  <div class="wrapper">
    <h2>Card #{{ num }}</h2>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Sed eaque fugit, ad quos itaque sunt harum aspernatur consequatur eligendi maxime!</p>
    <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Illum voluptas dolore ipsam maxime placeat!</p>
    <ButtonPrimary text="Do something cool" />
  </div>
</template>

<style scoped>
.wrapper {
  background-color: var(--color-blue-gray-050);
  border-radius: 6px;
  padding: 1rem;
}

h2 {
  font-weight: 500;
  margin-bottom: 2rem;
}

p {
  margin-bottom: 1rem;
}
</style>