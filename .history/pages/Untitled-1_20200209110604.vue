<template>
  <v-container fluid>
    <v-text-field
      v-model="searchText"
      placeholder="検索ワードを入力してください"
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
  mounted: function () {
    this.send('焼肉')
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
        .then((response) => {
          console.log(response)
          this.shops = response.data.rest
        })
    }
  },
  data: function () {
    return {
      searchText: '',
      shops: []
    }
  }
}
</script>