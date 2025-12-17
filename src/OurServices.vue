<template>
  <div class="grid sm:grid-cols-2 md:grid-cols-4 gap-7 my-25 px-10">
    <!-- Our Services -->
    <div class="pt-2">
      <div class="text-yellow-400 mb-5">Our Services</div>
      <div class="font-bold text-2xl">
        Experience Comfort, Conveinience, And Care
      </div>
    </div>

    <!-- Services Items -->
    <ServiceItem v-for="service in services"
      :title="service.title" :text="service.text"
    ></ServiceItem>
  </div>
</template>

<script>
import ServiceItem from './ServiceItem.vue';

  export default {
    components: {
      ServiceItem
    },
    data() {
      return {
        services: [
          {
            title: 'WIFI',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
          {
            title: 'Parking',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
          {
            title: 'Housekeeping',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
          {
            title: 'Laundry',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
          {
            title: 'Concierge',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
          {
            title: 'Breakfast',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
          {
            title: 'Gym',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
          {
            title: 'Spa',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
          {
            title: 'Shuttle',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
          {
            title: 'Security',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
          {
            title: 'Dining',
            text: 'Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque laudantium, totam rem aperiam, eaque ipsa'
          },
        ]
      };
    }
  }
</script>