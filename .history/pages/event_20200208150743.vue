<template>
  <div class="main">
    hello
    <v-btn height="50" loading x-small="" block >押してごらん</v-btn>
    <v-btn midium>押してごらん</v-btn>
    <v-btn x-large rounded color="info"　click=send>押してごらん</v-btn>
    <v-badge
      color="green"
      content="99"
    ></v-badge>
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
  conttent: {

  }

}
</script>