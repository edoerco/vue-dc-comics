<template>
  <div id="app">
    <Header />
    <Jumbotron />
    <Main />
    <Footer />
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Main from './components/Main.vue'
import Footer from './components/Footer.vue'
import Jumbotron from './components/Jumbotron.vue'



export default {
  name: 'App',
  components: {
    Header,
    Main,
    Footer,
    Jumbotron
  }
}
</script>

<style lang="scss">
  @import "./style/mixins";
  @import "./style/vars";

  // all'interno di generals ci stanno ordini generali
  @import "./style/generals";

</style>
