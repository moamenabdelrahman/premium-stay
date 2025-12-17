<template>
  <div class="flex px-10 gap-5 justify-center">
    <GalleryItem text="Balcony"></GalleryItem>
    <GalleryItem text="Pool"></GalleryItem>
    <GalleryItem text="Garden"></GalleryItem>
    <GalleryItem text="Lounge"></GalleryItem>
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