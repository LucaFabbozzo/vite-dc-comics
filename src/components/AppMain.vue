<script>
import AppCards from './AppCards.vue';
import books from '../data/books';
export default {
  name: "AppMain",
  components: { AppCards },
  data() {
    return {
      books,
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
      <div class="container cards">
        <AppCards v-for="(card, index) in books" :key="index"/>
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
  background-color: #1c1c1c;
  height: 50%;
  font-size: 0.6rem;
  .cards {
    display: flex;
    justify-content: space-between;
  }
}
.bottom {
  height: 50%;
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
