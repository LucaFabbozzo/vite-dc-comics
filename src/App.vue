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
  <App-header />
  <App-main />
  <App-footer />
</template>


<style>

</style>