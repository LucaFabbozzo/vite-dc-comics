<script>
export default {
  name: "AppMain",
  data() {
    return {
      menu: [
        {
          text: "Digital comics",
          img: "buy-comics-digital-comics.png",
          href: "#",
          current: false,
        },
        {
          text: "Dc merchandise",
          img: "buy-comics-merchandise.png",
          href: "#",
          current: false,
        },
        {
          text: "Subscription",
          img: "buy-comics-subscriptions.png",
          href: "#",
          current: false,
        },
        {
          text: "Comic shop locator",
          img: "buy-comics-shop-locator.png",
          href: "#",
          current: false,
        },
        {
          text: "Dc power visa",
          img: "buy-dc-power-visa.svg",
          href: "#",
          current: true,
        },
      ],
    };
  },
  methods: {
    getPathImage(img) {
      return new URL(`../assets/img/${img}`, import.meta.url).href;
    },
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
            <img :src="getPathImage(link.img)" alt="" />
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
  h1:after {
    content: "<--";
  }
  h1:before {
    content: "-->";
  }
}
.bottom {
  height: 115px;
  background-color: $tertiary-color;
  @include centerFlex;
  ul {
    @include betweenFlex;
    li {
      @include betweenFlex;
      list-style: none;
      img {
        width: 30px;
        margin-right: 10px;
      }
      .active {
        filter: invert(100%);
      }
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
