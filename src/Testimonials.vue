<template>
  <div class="px-10">
    <div class="text-yellow-400 mb-2">Testimonials</div>
    <div class="flex items-center mb-3">
      <div class="text-2xl font-bold me-auto">What Our Clients Say</div>
      <i class="fa-solid text-2xl fa-circle-arrow-left me-2" @click="goLeft"></i>
      <i class="fa-solid text-2xl fa-circle-arrow-right" @click="goRight"></i>
    </div>
    <!-- Carousel -->
    <div class="overflow-hidden mb-5">
      <div class="flex flex-nowrap transition-transform duration-300 ease-linear"
           :style="{ transform: `translateX(-${currentIndex * 50}%)` }"
      >
        <div class="h-50 w-1/2 shrink-0 px-2">
          <div class="h-full bg-gray-400"></div>
        </div>
        <div class="h-50 w-1/2 shrink-0 px-2">
          <div class="h-full bg-yellow-400"></div>
        </div>
        <div class="h-50 w-1/2 shrink-0 px-2">
          <div class="h-full bg-blue-400"></div>
        </div>
        <div class="h-50 w-1/2 shrink-0 px-2">
          <div class="h-full bg-green-400"></div>
        </div>
        <div class="h-50 w-1/2 shrink-0 px-2">
          <div class="h-full bg-black"></div>
        </div>
        <div class="h-50 w-1/2 shrink-0 px-2">
          <div class="h-full bg-white"></div>
        </div>
        <div class="h-50 w-1/2 shrink-0 px-2">
          <div class="h-full bg-purple-400"></div>
        </div>
        <div class="h-50 w-1/2 shrink-0 px-2">
          <div class="h-full bg-lime-200"></div>
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
      arr: [1,2,3,4,5,6,7,8],
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