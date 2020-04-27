<template>
  <div class="hello">
    <!-- <h1>简易demo</h1> -->
    <el-button type="primary" size='mini' @click="countReduce">-</el-button>
    <span>{{count}}</span>
    <el-button type="primary" size='mini' @click="countAdd">+</el-button>
  </div>
</template>

<script>
import { setup, reactive, computed, toRefs } from '@vue/composition-api'
export default {
      name: 'HelloWorld',
      created () {
        console.log('初始化created',2);
      },
      mounted () {
        console.log('初始化mounted',3);
      },
      setup(props, context) {
        console.log('初始化setup',1);
        // 生命周期，类似于created或者beforeCreate,在created方法前执行
        // props 中定义当前组件允许外界传递过来的参数名称, context相当于vue2.x中的this
        let state = reactive({
          // reactive就是定义data
          count: 0,
          double: computed(() => state.count * 2)
        })

        //方法
        let countReduce = ()=>{
          state.count--

        }
        let countAdd = ()=>{
          state.count++
        }
  
        return {
          ...toRefs(state), //...为浅拷贝，会影响数据响应式，通过toRefs可变为响应式数据
          countReduce,
          countAdd
        }
      }
}
</script>

<style scoped>
span{
  padding:0 10px
}
</style>
