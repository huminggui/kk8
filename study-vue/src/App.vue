<template>

  <div id="app">
    <button @click="goHome">父组件按钮</button>
      <hr>
    <child1 name="老胡" age="31"></child1>
    <hr>
    <child2></child2>
  </div>
</template>

<script>
import child1 from "./components/Child1"
import child2 from "./components/Child2"


export default {
  name: 'App',
  components: {
    child1,
    child2
  },
  methods:{
    goHome(){
      //回家吃饭的方法
     this.$children[0].eat();
      //第二个孩子是不吃饭
      this.$children[1].noEat();
    }
  }
}
</script>

<style>
#app {

}
</style>
