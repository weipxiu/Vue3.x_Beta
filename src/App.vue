<template>
  <div id="app">
    <Header></Header>
    <router-view />
    <Footer>
      </Footer>
  </div>
</template>

<script>
import Header from './components/header'
import Footer from './components/footer'

export default {
  components: {
    Header, Footer
  },
  name: 'App'
}
</script>


<style>
/* @import "./assets/css/style.css"; */
@import "https://www.weipxiu.com/wp-content/themes/boke/style.css";
</style>
