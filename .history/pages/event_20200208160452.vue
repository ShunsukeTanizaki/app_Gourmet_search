<template>
  <v-container fluid>
    <v-row>
      <v-col 
        cols="12"
        md="4">
        <v-row
          :align="alignment"
          :justify="justify"
          class="grey lighten-5"
          style="height: 300px;"
        >
          <EventCard v-for="shop in shops"
          v-bind:key="shop"
          >

          </EventCard>
        </v-row>
      </v-col>
      <v-col cols="12">
        <v-row justify="center">
          <v-col
            cols="6"
            md="2"
          >
            <v-select
              v-model="alignment"
              :items="alignmentsAvailable"
              label="Align"
            ></v-select>
          </v-col>

          <v-col
            cols="6"
            md="2"
          >
            <v-select
              v-model="justify"
              :items="justifyAvailable"
              label="Justify"
            ></v-select>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
  </v-container>
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
      shops: [1, 2, 3, 4, 5, 6],
      alignment: 'chenter',
      justify: 'start'
    }
  }
}
</script>