<script>
export default {
  name: "AppMain",
  data() {
    return {
      menu: [
        {
          text: "Digital comics",
          img: "../assets/img/buy-comics-digital-comics.png",
          href: "#",
          current: true,
        },
        {
          text: "Dc merchandise",
          img: "../assets/img/buy-comics-merchandise.png",
          href: "#",
          current: true,
        },
        {
          text: "Subscription",
          img: "../assets/img/buy-comics-shop-locator.png",
          href: "#",
          current: false,
        },
        {
          text: "Comic shop locator",
          img: "../assets/img/buy-comics-subscription.png",
          href: "#",
          current: false,
        },
        {
          text: "Dc power visa",
          img: "../assets/img/buy-dc-power-visa.svg",
          href: "#",
          current: false,
        },
      ],
    };
  },
};
</script>

<template>
  <main>
    <div class="top">
      <div class="container">
        <h1>Content goes here</h1>
      </div>
    </div>
    <div class="bottom">
      <div class="container menu">
        <ul>
          <li v-for="(link, index) in menu" :key="index">
            <a :href="link.href">{{ link.text }}</a>
          </li>
        </ul>
      </div>
    </div>
  </main>
</template>

<style lang="scss" scoped>
@use "../style/partials/mixin" as *;
@use "../style/partials/variables" as *;
.top {
  @include centerFlex;
  background-color: #1c1c1c;
  height: 100px;
  font-size: 0.6rem;
}
.bottom {
  height: 115px;
  background-color: $tertiary-color;
  @include centerFlex;
  ul {
    @include betweenFlex;
    li {
      list-style: none;
      a {
        text-decoration: none;
        color: $primary-color;
        font-size: 0.7rem;
        text-transform: uppercase;
      }
    }
  }
}
</style>
