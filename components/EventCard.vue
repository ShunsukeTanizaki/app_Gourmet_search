<template>
  <v-card
    class="mx-auto"
    max-width="400"
  >
    <v-img
      class="white--text align-end"
      height="200px"
      :src="shopItem.image_url.shop_image1"
    >
      <v-card-title class="shop-name">{{ shopItem.name }}</v-card-title>
    </v-img>

    <v-chip
      class="ma-2"
      color="pink"
      label
      text-color="white"
      small
      v-for="category_name in shopItem.code.category_name_s"
      v-bind:key="category_name"
    >
      <v-icon left>mdi-label</v-icon>
      {{ category_name }}
    </v-chip>

    <v-divider></v-divider>
    
    <v-card-text class="pt-0 pb-0">
      <div>{{ shopItem.pr.pr_short }}</div>
      
      <v-divider></v-divider>
      
      <div>{{ shopItem.address }}</div>
      
      <v-divider></v-divider>
      
      <div>{{ shopItem.tel }}</div>
    </v-card-text>

    <v-card-actions>
      <v-btn
        color="orange"
        :href="shopItem.url"
        target="blank"
      >
        詳細をみる
      </v-btn>
    </v-card-actions>
  </v-card>
</template>

<style scoped>
.shop-name {
  background-color: #111111BB
}
</style>

<script>
export default {
  props: ['shopItem']
}
</script>