  <script>
  export default {
    name: 'AppJumbo'
  }
  </script>

<template>
  <div class="jumbotron">
    <div class="container">
      <h3>Current Series</h3>
    </div>
  </div>
  
</template>


<style lang="scss" scoped>
@use '../style/partials/variables' as *;
 .jumbotron {
  height: 350px;
  background-image: url('../assets/img/jumbotron.jpg');
  background-size: cover;
  h3 {
    background-color: $tertiary-color;
    display: inline-block;
    text-align: center;
    text-transform: uppercase;
    padding: 10px 20px;
    transform: translateY(770%);
  }
 }
</style>