<template>
  <div class="flex px-10 gap-10 mb-25">
    <div class="w-110 h-100 bg-[url('../assets/whychooseus.png')] bg-cover shrink-0"></div>
    <div class="grow">
      <div class="text-yellow-400 text-2xl">Why Choose Us</div>
      <div class="font-bold text-3xl mb-5">Unmatched Quality, Trust, And Service</div>
      <div v-for="item in faqs" :id="item.id" @click="handleClick(item.id)"
        class="p-2 bg-gray-300 mb-2"
      >
        <div class="flex justify-between items-center">
          <span class="font-bold">{{ item.question }}</span>
          <i v-if="openedQuestionId === item.id" class="fa-solid fa-angle-right"></i>
          <i v-else class="fa-solid fa-angle-down"></i>
        </div>
        <div v-if="item.id === openedQuestionId"
          class="mt-2"
        >{{ item.answer }}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      faqs: [
        {
          id: '1',
          question: 'What amenities are included?',
          answer: 'some very random answer'
        },
        {
          id: '2',
          question: 'Is breakfast included?',
          answer: 'some very random answer'
        },
        {
          id: '3',
          question: 'Are pets allowed?',
          answer: 'some very random answer'
        },
        {
          id: '4',
          question: 'How can I book?',
          answer: 'some very random answer'
        }
      ],
      openedQuestionId: null
    };
  },
  methods: {
    handleClick(id) {
      if(this.openedQuestionId === id) {
        this.openedQuestionId = null;
      }
      else {
        this.openedQuestionId = id;
      }
    }
  }
}
</script>

<style scoped>
@reference "tailwindcss";
</style>