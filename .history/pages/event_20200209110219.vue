<template>
  <v-container fluid>
    <v-text-field
      v-model="searchText"
      solo-inverted
      flat
      hide-details
      label="Search"
      prepend-inner-icon="search"
      @change="search"
    />
    <v-row >
      <v-col 
        cols="12" 
        xs="12" 
        sm="6" 
        md="4" 
        lg="3" 
        xl="3"
        v-for="shop in shops" v-bind:key="shop.id"
      >
        <EventCard v-bind:shop-item="shop"></EventCard>
      </v-col>
    </v-row>
    <v-btn @click="send">クリック</v-btn>
  </v-container>
</template>

<script>
import axios from 'axios'
import EventCard from '@/components/EventCard'
export default {
  layout: 'admin',
  components: {
    EventCard
  },
  methods: {
    search: function () {
      this.send(this.searchText)
    },
    send: function (searchText) {
      let baseUrl = 'https://api.gnavi.co.jp/RestSearchAPI/v3/'
      let apiKey = '60e919407001d7a00adc7f4a8764a2d9'
      let limit = 30
      let url = `${baseUrl}?keyid=${apiKey}&freeword=${searchText}&hit_per_page=${limit}`
      axios
        .get(url)
        .then((res) => {
          this.shops = res.data.rest
        })
    }
  },
  data: function (searchText) {
    return {
      shops: [
        {
          id: 1,
          name: '焼肉 長谷川1',
          image_url: 'http://uds.gnst.jp/rest/img/me02ncv80000/s_00im.jpg?t=1395807984'
        },
        {
          id: 2,
          name: '焼肉 長谷川1',
          image_url: 'http://uds.gnst.jp/rest/img/me02ncv80000/s_00im.jpg?t=1395807984'
        },
        {
          id: 3,
          name: '焼肉 長谷川1',
          image_url: 'http://uds.gnst.jp/rest/img/me02ncv80000/s_00im.jpg?t=1395807984'
        },
        {
          id: 4,
          name: 'タピオカ',
          image_url: 'http://uds.gnst.jp/rest/img/me02ncv80000/s_00im.jpg?t=1395807984'
        }
      ]
    }
  }
}
</script>