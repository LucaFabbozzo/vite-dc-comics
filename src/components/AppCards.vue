  <script>
  export default {
  name: 'AppCards',
  props: {
    cardThumb: String,
    cardSeries: String
    }
  }
  </script>

<template>
  <div class="card">
    <img :src="cardThumb" :alt="cardSeries">
    <h4>{{cardSeries}}</h4>
  </div>
</template>


<style lang="scss" scoped>
@use '../style/partials/variables' as *;
  .card {
    padding: 10px;
    width: 150px;
    height: 150px;
    img {
      width: 100%;
      height: 100%;
      object-fit: cover scale-down;
    }
    h4 {
      color: $primary-color;
    }
  }


</style>