<script>
export default {
  name: "AppHeader",
};
</script>

<template>
  <div class="up"></div>
  <div class="container">
    <header>
      <div class="logo">
        <img src="/dc-logo.png" alt="Logo" />
      </div>
      <nav>
        <ul>
          <li><a href="#">Characters</a></li>
          <li><a href="#">Comics</a></li>
          <li><a href="#">Movies</a></li>
          <li><a href="#">Tv</a></li>
          <li><a href="#">Games</a></li>
          <li><a href="#">Collectibles</a></li>
          <li><a href="#">Videos</a></li>
          <li><a href="#">Fans</a></li>
          <li><a href="#">News</a></li>
          <li><a href="#">Show</a></li>
        </ul>
      </nav>
    </header>
  </div>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.up {
  height: 30px;
  background-color: $secondary-color;
}
header {
  @include betweenFlex;
  height: 85px;
  background-color: $primary-color;
  img {
    width: 50px;
  }
  ul {
    list-style: none;
    @include centerFlex;
  }
  li {
    margin-left: 20px;
    text-transform: uppercase;
    font-size: 0.6rem;
    font-weight: bold;
  }
  a {
    text-decoration: none;
    $secondary-color: #303030;
  }
}
</style>
