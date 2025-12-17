<template>
  <div class="h-1500 bg-red-400">
    <Navbar></Navbar>
    <Hero></Hero>
  </div>
</template>

<script>
import Hero from './Hero.vue';
import Navbar from './Navbar.vue';

export default {
  components: {
    Navbar,
    Hero
  }
}
</script>

<style scoped></style>