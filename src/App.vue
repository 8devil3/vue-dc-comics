<template>
  <div id="app">
    <HeaderSite />
    <MainSite />
    <BlueIcons />
    <FooterSite />
  </div>
</template>

<script>
import BlueIcons from './components/BlueIcons.vue'
import FooterSite from './components/FooterSite.vue'
import HeaderSite from './components/HeaderSite.vue'
import MainSite from './components/MainSite.vue'

export default {
  name: 'App',
  components: {
    HeaderSite,
    MainSite,
    FooterSite,
    BlueIcons
  }
}
</script>

<style lang="scss">
@import './assets/scss/import-styles.scss'
</style>
