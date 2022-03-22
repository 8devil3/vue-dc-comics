<template>
  <div id="app">
    <HeaderSite />
    <MainSite />
    <FooterSite />
  </div>
</template>

<script>
import HeaderSite from './components/HeaderSite.vue'
import MainSite from './components/MainSite.vue'
import FooterSite from './components/FooterSite.vue'

export default {
  name: 'App',
  components: {
    HeaderSite,
    MainSite,
    FooterSite
  }
}
</script>

<style lang="scss">
@import './assets/scss/import-styles.scss'
</style>
