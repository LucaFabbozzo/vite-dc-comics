<script>
import AppCards from './AppCards.vue';
import books from '../data/books';
import Items from '../components/Items.vue'
export default {
  name: "AppMain",
  components: { AppCards, Items },
  data() {
    return {
      books,
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
    <Items />
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
</style>
