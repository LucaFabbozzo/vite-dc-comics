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
    flex-basis: 25%;
    min-height: 200px;
  }


</style>