<template>
  <div class="fixed w-280 z-100 transition-all duration-300"
      :class="{
        'bg-white shadow-md': scrolled,
        'bg-transparent': !scrolled
      }"
  >
    <div class="flex px-10 h-25 items-center"
        :class="{
          'text-white': !scrolled
        }"
    >
      <div class="pressable text-[35px] font-[Playfair_Display_SC] mr-10">LOGO</div>
      <div class="flex gap-13 ms-15 font-[EB_Garamond] text-[18px]">
        <div class="pressable">Home</div>
        <div class="pressable">Services</div>
        <div class="pressable">About us</div>
        <div class="pressable">Contact us</div>
        <div class="pressable">Location</div>
      </div>
      <button type="button" class="ms-auto pressable px-2.5 py-1.5 "
                           :class="{
                            'bg-white text-black': !scrolled,
                            'bg-black text-white': scrolled
                           }"
      >
        Book Now
      </button>

      <!-- Dark Mode Toggle -->
      <button
        @click="toggleDarkMode"
        class="ml-4 px-2 py-1 border rounded transition"
      >
        {{ darkMode ? 'Light' : 'Dark' }}
      </button>
      
    </div>
    <div class="border border-neutral-200/30 w-93/100 mx-auto">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      scrolled: false,
      darkMode: false
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  beforeUnmount() {
    window.removeEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      this.scrolled = window.scrollY > 20
    },
    toggleDarkMode() {
      this.darkMode = !this.darkMode;
      this.applyDarkMode();
    },
    applyDarkMode() {
      if (this.darkMode) {
        // document.documentElement.classList.add('dark');
      } else {
        // document.documentElement.classList.remove('dark');
      }
    }
  }
}
</script>

<style scoped>
@reference "tailwindcss";

.pressable { @apply
  hover:cursor-pointer
}
</style>