<template>
  <div id="app">
    <Header />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/MainHeader.vue'
import Main from './components/MainContent.vue'
import Footer from './components/MainFooter.vue'

export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
  }
}
</script>

<style lang="scss">
@import './assets/scss/common.scss';

#app {
  // font-family: Avenir, Helvetica, Arial, sans-serif;
  // font-family:"Arial Rounded MT Bold", sans-serif;
  font-family: 'Nunito', sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
</style>
