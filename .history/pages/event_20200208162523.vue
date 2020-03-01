<template>
  <v-container fluid>
    <v-row >
      <v-col 
        cols="12" 
        xs="12" 
        sm="6" 
        md="4" 
        lg="3" 
        xl="3"
        v-for="shop in shops" v-bind:key="shop"
      >
        <EventCard></EventCard>
      </v-col>
    </v-row>
  </v-container>
</template>

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
      shops: [
        {
          name: 'yakimniku',
          image_url: "https://imgfp.hotp.jp/IMGH/09/47/P028840947/P028840947_480.jpg"
        },
        {
          name: 'yakimniku',
          image_url: "https://imgfp.hotp.jp/IMGH/09/47/P028840947/P028840947_480.jpg"
        },
        {
          name: 'yakimniku',
          image_url: "https://imgfp.hotp.jp/IMGH/09/47/P028840947/P028840947_480.jpg"
        },
        ],
      alignment: 'center',
      justify: 'start'
    }
  }
}
</script>