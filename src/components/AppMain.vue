<script>
import AppCards from './AppCards.vue';
import books from '../data/books';
import menu from '../data/menu';
export default {
  name: "AppMain",
  components: { AppCards },
  data() {
    return {
      books,
      menu
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
        <AppCards
          v-for="(card, index) in books" 
          :key="index"
          :cardThumb="card.thumb"
          :cardSeries="card.series"
          />
         
      </div> 
      <div class="btn">
        <a href="#">Load More</a>
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
  padding-top: 30px;
  padding-bottom: 10px;
  background-color: #1c1c1c;
  height: 50%;
  font-size: 0.6rem;
  .cards {
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: space-between;
  }
  .btn {
    margin: 50px auto;
    width: 150px;
    text-align: center;
    background-color: $tertiary-color;
    padding: 10px 15px;
    cursor: pointer;
    a {
      color: $primary-color;
      text-decoration: none;
      text-transform: uppercase;
    }
  }
  
}
.bottom {
  height: 120px;
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
