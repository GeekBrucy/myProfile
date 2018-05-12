<template>
  <div id="app">
    <home-header></home-header>
    <div class="pg-content">
      <router-view/>
    </div>
    <home-footer></home-footer>
  </div>
</template>

<script>
import HomeHeader from './pages/Home/components/Header'
import HomeFooter from './pages/Home/components/Footer'
export default {
  name: 'App',
  components: {
    HomeHeader,
    HomeFooter
  }
}
</script>

<style lang="stylus" scoped>
#app
  min-height 100%
  position relative
</style>
