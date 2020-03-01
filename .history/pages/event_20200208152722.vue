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
        src="https://www.google.com/imgres?imgurl=http%3A%2F%2Fimg01.naganoblog.jp%2Fusr%2Fy%2Fa%2Fm%2Fyamazaki%2FIMGP5568.JPG&imgrefurl=http%3A%2F%2Fyamazaki.naganoblog.jp%2Fe1806342.html&tbnid=pbriYeVmlrw1AM&vet=12ahUKEwjh2qbi9LvnAhWYCN4KHaOpDIAQMygWegQIARAw..i&docid=1IrzsAmM587IeM&w=450&h=300&q=%E9%9D%B4%E3%80%80%E3%82%AA%E3%83%BC%E3%83%80%E3%83%BC%E5%B0%82%E9%96%80&ved=2ahUKEwjh2qbi9LvnAhWYCN4KHaOpDIAQMygWegQIARAw"
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