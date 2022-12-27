<script>
import menu from '../data/menu';
  export default {
  name: 'Items',
    data() {
      return {
        menu
      }
    },
  methods: {
      getPathImage(img) {
        return new URL(`../assets/img/${img}`, import.meta.url).href;
      },
    }
  }
  </script>

<template>
  <div class="items">
    <div class="container">
      <ul>
        <li v-for="(item, index) in menu" :key="index">
          <img :src="getPathImage(item.img)" :alt="item.text">
          <a :href="item.href">{{item.text}}</a>
        </li>
      </ul>
    </div>
  </div>
</template>


<style lang="scss">
@use '../style/partials/variables' as *;
@use '../style/partials/mixin' as *;
.items {
  height: 120px;
  background-color: $tertiary-color;
  display: flex;
  align-items: center;
  .container{
    ul {
      @include betweenFlex;
      li {
        @include startFlex;
        align-items: center;
        img {
          width: 40px;
          margin-right: 10px;
        }
        a {
          text-decoration: none;
          color: $primary-color;
          text-transform: uppercase;
          font-size: 0.6rem;
        }
      }
    }
  }
}
</style>