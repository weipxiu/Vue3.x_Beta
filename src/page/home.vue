<template>
  <div class="continar">
    <List></List>
    <Sidebar></Sidebar>
  </div>
</template>

<script>
import List from '../components/list'
import Sidebar from '../components/sidebar'

export default {
  components: {
    List, Sidebar
  },
  name: 'home',
  data() {
    return {
      msg: 'Welcome to Your Vue.js App'
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>

</style>
