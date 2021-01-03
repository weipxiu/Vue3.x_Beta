<template>
  <div class="home">
    <p>初始值： {{sum}}
    </p>
    <p> 计算数字：{{sum_calc}}
    </p>
    <p @click="changSum">点击改变{{sum}}</p>
  </div>
</template>

<script>
// import HelloWorld from '@/components/HelloWorld.vue'
import { reactive, toRefs, computed } from 'vue';
export default {
  name: 'Home',
  components: {
    // HelloWorld
  },
  setup() {
    const state = reactive({
      sum: 1,
      sum_calc: computed(() => {
        return state.sum + 5
      })
    })

    const methods = {
      changSum: () => {
        state.sum += 1
      }
    }
    return {
      ...toRefs(state),
      ...methods
    }
  }
}
</script>
