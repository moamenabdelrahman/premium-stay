<template>
  <div class="h-1500 bg-red-400">
    <Navbar></Navbar>
    <Hero></Hero>
    <AboutUs></AboutUs>
    <Gallery></Gallery>
    <OurServices></OurServices>
  </div>
</template>

<script>
import AboutUs from './AboutUs.vue';
import Gallery from './Gallery.vue';
import Hero from './Hero.vue';
import Navbar from './Navbar.vue';
import OurServices from './OurServices.vue';

export default {
  components: {
    Navbar,
    Hero,
    AboutUs,
    Gallery,
    OurServices
  }
}
</script>

<style scoped></style>