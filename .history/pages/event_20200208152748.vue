<template>
  <div class="main">
    <v-card
      class="mx-auto"
      max-width="400"
      v-for="shop in shops"
      v-bind:key="shop"
    >
      <v-img
        class="white--text align-end"
        height="200px"
        src="https://lh3.googleusercontent.com/proxy/Gi9pNK_eg_EPY78-ULwcXxmhJITXwKK_MVm-RPmrcnvFeuIGR1ssAkAmD6b377uQzT9n8UtDA_S7MHyB8Q9nPZ5nDRrWKyJcqrqxxTA"
      >
        <v-card-title>Top 10 Australian beaches</v-card-title>
      </v-img>
  
      <v-card-subtitle class="pb-0">Number 10</v-card-subtitle>
  
      <v-card-text class="text--primary">
        <div>Whitehaven Beach</div>
  
        <div>Whitsunday Island, Whitsunday Islands</div>
      </v-card-text>
  
      <v-card-actions>
        <v-btn
          color="orange"
          text
        >
          Share
        </v-btn>
  
        <v-btn
          color="orange"
          text
        >
          Explore
        </v-btn>
      </v-card-actions>
    </v-card>
    </div>
</template>

<style scoped>
  /* div {
    color: red;
  }
  .main {
    font-size: x-large;
  } */
</style>

<script>
export default {
  layout: 'admin',
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