<template>
  <div class="h-80 w-40 max-w-60 bg-cover shrink-0 grow flex justify-center items-center font-bold"
      :style="{ backgroundImage: `url(${imageUrl})` }"
  >
  </div>
</template>

<script>
export default {
  props: ['imageUrl']
}
</script>