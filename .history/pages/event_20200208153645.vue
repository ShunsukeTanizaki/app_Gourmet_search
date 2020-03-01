<template>
  <div class="main">
    
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