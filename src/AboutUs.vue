<template>
  <div class="flex gap-4 py-25 px-15">
    <!-- Experience -->
    <div class="border-4 border-yellow-400 flex py-7 shrink-0 relative h-fit">
      <div class="bg-red-400 w-25 h-5 absolute top-0 left-1/2 -translate-x-1/2 -translate-y-1/2"></div>
      <div class="text-5xl font-bold ms-5 me-2">35</div>
      <div class="me-2">years <br> of experience</div>
      <div class="bg-red-400 w-25 h-5 absolute bottom-0 left-1/2 -translate-x-1/2 translate-y-1/2"></div>
    </div>

    <!-- About us -->
    <div class="mx-5 w-70 shrink-0">
      <div class="text-yellow-400 text-2xl mb-2">About Us</div>
      <div class="font-bold text-2xl">Who We Are: Crafting Memorable Stays, One Destination At A Time</div>
    </div>

    <!-- Message -->
    <div class="max-h-60 overflow-hidden">
      {{ message }}
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: 'At our core, we believe that every journey deserves a place that feels like home. With a passion for quality and personalized experiences, we carefully curate a selection of stays that cater to every traveler’s needs, from cozy retreats to luxury escapes. Our commitment is to provide not just a place to stay, but a destination where memories are made, ensuring comfort, convenience, and an exceptional experience at every step of your journey.'
    };
  }
}
</script>

<style scoped>
@reference "tailwindcss";

</style>