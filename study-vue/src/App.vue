<template>

  <div id="app">


    <h1>测试</h1>
    {{showCourse}}

    <button @click="change">change</button>
  </div>
</template>

<script>

export default {
  name: 'App',
  //父组件中提供变量，孩子组件最深的也可以获取。
  provide(){
    return{
      foot:"foooooot",

    }
  },
  data(){
    return {
      value:"default",
      course:[{name:"张三"},{name:"李四"},{name:"王五"}],
      showCourse:""
      
    }
  },
  watch:{
    course:{
      immediate:true,
      deep:true,
      handler(newValue){
        console.log("1111111");
        this.showCourse=newValue.length+"门课";
      }
    }
  },
  components: {

  },
  methods:{
    change(){
      this.course[0].name="赵六";
    }
    


  }



}
</script>

<style>
#app {

}
</style>
