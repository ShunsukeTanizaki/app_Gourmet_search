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
      {{ shop.name }}
      {{ shop.image_url }}
        <EventCard v-bind:
        shop-item="shop"></EventCard>
      </v-col>
    </v-row>
    <v-btn>クリック</v-btn>
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
      axios.get('https://api.gnavi.co.jp/RestSearchAPI/v3/?keyid=60e919407001d7a00adc7f4a8764a2d9&freeword=%E7%84%BC%E8%82%89')
        .then((res) => {
        console.log('res')
        }
      )
    }
  },
  data: function () {
    return {
      shops: [
        {
          name: '焼肉　1',
          image_url: 'https://imgfp.hotp.jp/IMGH/09/47/P028840947/P028840947_480.jpg'
        },
        {
          name: '焼肉　2',
          image_url: 'https://imgfp.hotp.jp/IMGH/09/47/P028840947/P028840947_480.jpg'
        },
        {
          name: '焼肉　3',
          image_url: 'https://imgfp.hotp.jp/IMGH/09/47/P028840947/P028840947_480.jpg'
        }
      ]
    }
  }
}
</script>