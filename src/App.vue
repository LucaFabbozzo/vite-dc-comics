<script>
import AppFooter from './components/AppFooter.vue'
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
export default {
  name: 'App',
  components: { AppHeader, AppMain, AppFooter },
  
}
</script>

<template>
  <div class="container">
    <App-header />
    <App-main />
    <App-footer />
  </div>
</template>


<style lang="scss">
  @use './style/general';
</style>