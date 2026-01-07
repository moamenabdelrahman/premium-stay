<template>
  <div class="flex px-10 gap-5 justify-center">
    <GalleryItem image-url="../assets/balcony.png"></GalleryItem>
    <GalleryItem image-url="../assets/pool.png"></GalleryItem>
    <GalleryItem image-url="../assets/garden.png"></GalleryItem>
    <GalleryItem image-url="../assets/lounge.png"></GalleryItem>
  </div>
</template>

<script>
import GalleryItem from './GalleryItem.vue';

export default {
  components: {
    GalleryItem
  }
}
</script>