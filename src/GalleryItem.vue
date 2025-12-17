<template>
  <div class="h-80 w-40 max-w-60 shrink-0 grow bg-gray-400 flex justify-center items-center font-bold">
    {{ text }}
  </div>
</template>

<script>
export default {
  props: ['text']
}
</script>