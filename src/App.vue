<template>
  <div class="h-1500 bg-red-400">
    <Navbar></Navbar>
    <Hero></Hero>
    <AboutUs></AboutUs>
  </div>
</template>

<script>
import AboutUs from './AboutUs.vue';
import Hero from './Hero.vue';
import Navbar from './Navbar.vue';

export default {
  components: {
    Navbar,
    Hero,
    AboutUs
  }
}
</script>

<style scoped></style>