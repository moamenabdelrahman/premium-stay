<template>
  <div class="flex px-10 gap-10 mb-25">
    <div class="w-110 h-100 bg-[url('../assets/whychooseus.png')] bg-cover shrink-0"></div>
    <div class="grow">
      <div class="text-yellow-400 mb-4 text font-[Raleway]">Why Choose Us</div>
      <div class="font-bold text-xl mb-5 font-[Fraunces] dark:text-white">Unmatched Quality, Trust, And Service</div>
      <div v-for="item in faqs" :id="item.id" @click="handleClick(item.id)"
        class="px-6 py-2 bg-neutral-200 dark:bg-[#373A40] mb-4 font-sans dark:text-white"
      >
        <div class="flex justify-between items-center">
          <span class="text-sm">{{ item.question }}</span>
          <i v-if="openedQuestionId === item.id" class="fa-solid fa-angle-right"></i>
          <i v-else class="fa-solid fa-angle-down"></i>
        </div>
        <div v-if="item.id === openedQuestionId"
          class="mt-4 text-[12px]"
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
          answer: 'Booking is easy through our website or mobile app. Simply choose your dates, select your stay, and complete the reservation process'
        },
        {
          id: '2',
          question: 'Is breakfast included?',
          answer: 'Booking is easy through our website or mobile app. Simply choose your dates, select your stay, and complete the reservation process'
        },
        {
          id: '3',
          question: 'Are pets allowed?',
          answer: 'Booking is easy through our website or mobile app. Simply choose your dates, select your stay, and complete the reservation process'
        },
        {
          id: '4',
          question: 'How can I book?',
          answer: 'Booking is easy through our website or mobile app. Simply choose your dates, select your stay, and complete the reservation process'
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