<template>
  <div class="fixed w-full">
    <div class="flex px-10 h-25 items-center">
      <div class="pressable text-2xl">LOGO</div>
      <div class="flex gap-8 ms-15">
        <div class="pressable">Home</div>
        <div class="pressable">Services</div>
        <div class="pressable">About us</div>
        <div class="pressable">Contact us</div>
        <div class="pressable">Location</div>
      </div>
      <button type="button" class="ms-auto pressable bg-white px-2.5 py-1.5">Book Now</button>
    </div>
    <div class="border w-85/100 mx-auto">
    </div>
  </div>
</template>

<script>
export default {

}
</script>

<style scoped>
@reference "tailwindcss";

.pressable { @apply
  hover:cursor-pointer
}
</style>