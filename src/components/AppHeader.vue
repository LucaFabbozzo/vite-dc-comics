<script>
import nav from '../data/nav';
export default {
  name: "AppHeader",
  data() {
    return {
      nav
    };
  },
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
          <li v-for="(link, index) in nav" :key="index">
            <a :class="{ active: link.current }" :href="link.href">{{
              link.text
            }}</a>
          </li>
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
  background-color: #212121;
}
header {
  @include aroundFlex;
  height: 85px;
  background-color: $primary-color;
  img {
    width: 50px;
    cursor: pointer;
  }
  ul {
    list-style: none;
    @include aroundFlex;
    width: 600px;
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
    padding-bottom: 34px;
  }

  // .active {
  //   color: $tertiary-color;
  //   border-bottom: 3px solid $tertiary-color;
  // }

  a:hover {
    color: $tertiary-color;
    border-bottom: 3px solid $tertiary-color;
  }
}
</style>
