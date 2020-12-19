<template>
    <div>
        child2 component {{name}}
        <button @click="emitChild2">点击组件2传值组件1</button>
    </div>
</template>
<script>
export default {
    data(){
        return{
            
        }
    },
    methods:{
        emitChild2(){
            //child1向child2发起命令
            this.$parent.$emit("child2ToChild1");
        },
        noEat(){
            console.log("不回家吃饭...");
        }
    }
}
</script>
<style scoped>

</style>