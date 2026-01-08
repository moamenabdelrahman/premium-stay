<template>
  <div class="h-screen text-white py-4 bg-yellow-100 flex flex-col items-center bg-cover bg-[url(../assets/hero.png)]">
    <div class="font-bold font-[Roslindale] text-[40px] mb-3 mt-auto">
      {{ header }}
    </div>
    <div class="font-sans text-[23px]">
      {{ text }}
    </div>
    <i class="mt-auto pressable fa-solid fa-angle-down"></i>
  </div>
</template>

<script>
  export default {
    data() {
      return {
        header: 'Find Your Perfect Stay - Unwind In Comfort, Anywhere',
        text: 'Discover Handpicked Stays That Combine Comfort, Style, And Unforgettable Experiences.'
      };
    }
  }
</script>

<style scoped>
@reference "tailwindcss";

.pressable { @apply
  hover:cursor-pointer
}
</style>