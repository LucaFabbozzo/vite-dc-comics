<script>
export default {
  name: "AppHeader",
  data() {
    return {
      menu: [
        {
          text: "Characters",
          href: "#",
          current: false,
        },
        {
          text: "Comics",
          href: "#",
          current: true,
        },
        {
          text: "Movies",
          href: "#",
          current: false,
        },
        {
          text: "Tv",
          href: "#",
          current: false,
        },
        {
          text: "Games",
          href: "#",
          current: false,
        },
        {
          text: "Collectibles",
          href: "#",
          current: false,
        },
        {
          text: "Videos",
          href: "#",
          current: false,
        },
        {
          text: "Fans",
          href: "#",
          current: false,
        },
        {
          text: "News",
          href: "#",
          current: false,
        },
        {
          text: "Show",
          href: "#",
          current: false,
        },
      ],
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
          <li v-for="(link, index) in menu" :key="index">
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
  .active {
    color: $tertiary-color;
  }
}
</style>
