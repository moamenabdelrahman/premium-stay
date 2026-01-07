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
      <div class="pressable text-2xl">LOGO</div>
      <div class="flex gap-8 ms-15">
        <div class="pressable">Home</div>
        <div class="pressable">Services</div>
        <div class="pressable">About us</div>
        <div class="pressable">Contact us</div>
        <div class="pressable">Location</div>
      </div>
      <button type="button" class="ms-auto pressable px-2.5 py-1.5"
                           :class="{
                            'bg-white text-black': !scrolled,
                            'bg-black text-white': scrolled
                           }"
      >
        Book Now
      </button>
    </div>
    <div class="border border-neutral-200/30 w-85/100 mx-auto">
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      scrolled: false
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