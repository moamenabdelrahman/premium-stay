<template>
  <div class="overflow-hidden bg-neutral-100 dark:bg-[#23262D] w-280 mx-auto border-x">
    <Navbar></Navbar>
    <Hero></Hero>
    <AboutUs></AboutUs>
    <Gallery></Gallery>
    <OurServices></OurServices>
    <WhyChooseUs></WhyChooseUs>
    <Testimonials></Testimonials>
    <ServiceAreas></ServiceAreas>
    <Footer></Footer>
  </div>
</template>

<script>
import AboutUs from './AboutUs.vue';
import Footer from './Footer.vue';
import Gallery from './Gallery.vue';
import Hero from './Hero.vue';
import Navbar from './Navbar.vue';
import OurServices from './OurServices.vue';
import ServiceAreas from './ServiceAreas.vue';
import Testimonials from './Testimonials.vue';
import WhyChooseUs from './WhyChooseUs.vue';

export default {
  components: {
    Navbar,
    Hero,
    AboutUs,
    Gallery,
    OurServices,
    WhyChooseUs,
    Testimonials,
    ServiceAreas,
    Footer
  }
}
</script>

<style scoped></style>