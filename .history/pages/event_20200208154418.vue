<template>
  <div class="main">
    <EventCard
      v-for="shop in shops"
    ></EventCard>
    </div>
</template>

<style scoped>
</style>

<script>
import EventCard from '@/components/EventCard'

export default {
  layout: 'admin',
  components: {
    EventCard
  },
  methods: {
    send: function () {
      alert('hello')
    }
  },
  data: function () {
    return {
      shops: [1, 2, 3, 4, 5]
    }
  }
}
</script>