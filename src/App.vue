<template>
  <div id="app">
    <HeaderDcComics />
    <MainContent />
    <FooterDcComics />

  </div>
</template>

<script>
import HeaderDcComics from './components/HeaderDcComics.vue'
import MainContent from './components/MainContent.vue'
import FooterDcComics from './components/FooterDcComics.vue'

export default {
  name: 'App',
  components: {
    HeaderDcComics,
    MainContent,
    FooterDcComics
  }
}
</script>

<style lang="scss">
@import "./assets/styles/style.scss";
</style>
