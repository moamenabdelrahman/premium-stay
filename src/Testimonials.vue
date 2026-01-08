<template>
  <div class="px-10">
    <div class="text-yellow-400 mb-4 font-[Raleway]">Testimonials</div>
    <div class="flex items-center mb-7">
      <div class="text-2xl font-bold me-auto font-[Fraunces]">What Our Clients Say</div>
      <i class="fa-solid text-2xl fa-circle-arrow-left me-2" @click="goLeft"></i>
      <i class="fa-solid text-2xl fa-circle-arrow-right" @click="goRight"></i>
    </div>
    <!-- Carousel -->
    <div class="overflow-hidden mb-10">
      <div class="flex flex-nowrap transition-transform duration-300 ease-linear"
           :style="{ transform: `translateX(-${currentIndex * 50}%)` }"
      >
        <!-- Testimonials -->
        <div v-for="testimonial in arr" class="h-50 w-1/2 shrink-0 px-2">
          <div class="h-full bg-neutral-200 flex px-5 py-7">
            <div class="w-15 h-15 shrink-0 border-2 rounded-full overflow-hidden mr-5">
              <img :src="testimonial.url">
            </div>
            <div>
              <div class="font-sans font-bold text-2xl mb-1">{{ testimonial.name }}</div>
              <div class="text-sm mb-2">Local Guide <span class="ml-2 font-bold">27 reviews</span></div>
              <div class="text-[12px] mb-4">
                <i v-for="_ in 5" class="fa-solid fa-star" style="color: #fea500;"></i>
                <span class="ml-3">6 months ago</span>
              </div>
              <div class="font-sans text-[14px]">
                {{ testimonial.comment }}
              </div>
            </div>
            <div class="w-10 h-10 shrink-0 rounded-full overflow-hidden">
              <img src="../assets/google.png">
            </div>
          </div>
        </div>
      </div>
    </div>
    <!-- Dots -->
    <div class="flex items-center gap-1.5 justify-center">
      <i v-for="_ in currentIndex" class="fa-solid d-block text-[#1D1D1D]/21 fa-circle"></i>
      <svg width="50" height="17" viewBox="0 0 37 11" fill="none" xmlns="http://www.w3.org/2000/svg">
        <rect width="36" height="11" rx="5.5" fill="#1D1D1D"/>
      </svg>
      <i v-for="_ in (arr.length - currentIndex - 2)" class="fa-solid text-[#1D1D1D]/21 fa-circle"></i>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      arr: [
        { name: 'Stephen', comment: 'The service was impeccable, the amenities were top-notch, and the room was incredibly comfortable', url: '../assets/testimonial.avif' },
        { name: 'Robert', comment: 'The attention to detail in the rooms and the welcoming atmosphere made my stay memorable.', url: '../assets/testimonial2.jfif' },
        { name: 'Stephen', comment: 'The service was impeccable, the amenities were top-notch, and the room was incredibly comfortable', url: '../assets/testimonial.avif' },
        { name: 'Robert', comment: 'The attention to detail in the rooms and the welcoming atmosphere made my stay memorable.', url: '../assets/testimonial2.jfif' },
        { name: 'Stephen', comment: 'The service was impeccable, the amenities were top-notch, and the room was incredibly comfortable', url: '../assets/testimonial.avif' },
        { name: 'Robert', comment: 'The attention to detail in the rooms and the welcoming atmosphere made my stay memorable.', url: '../assets/testimonial2.jfif' },
      ],
      currentIndex: 0
    };
  },
  methods: {
    goRight() {
      if(this.currentIndex + 2 < this.arr.length) {
        this.currentIndex++;
      }
    },
    goLeft() {
      if(this.currentIndex > 0) {
        this.currentIndex--;
      }
    }
  }
}
</script>