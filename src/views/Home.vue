<template>
  <div class="home">
    {{sum}}
  </div>
</template>

<script>
// import HelloWorld from '@/components/HelloWorld.vue'
import { reactive } from 'vue';
export default {
  name: 'Home',
  components: {
    // HelloWorld
  },
  setup() {
    const state = reactive({
      sum: 1
    })
    return {
      ...state
    }
  }
}
</script>
