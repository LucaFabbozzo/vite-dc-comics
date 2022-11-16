<script>
import AppFooter from './components/AppFooter.vue'
import AppHeader from './components/AppHeader.vue'
import AppMain from './components/AppMain.vue'
import AppJumbo from './components/AppJumbo.vue'
export default {
  name: 'App',
  components: { AppHeader, AppMain, AppFooter, AppJumbo },
  
}
</script>

<template>
    <AppHeader />
    <AppJumbo />
    <AppMain />
    <AppFooter />
</template>


<style lang="scss">
  @use './style/general';
</style>