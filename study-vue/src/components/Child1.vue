<template>
    <div>
        <h3 v-on="$listeners">调用父类的毁掉函数</h3>
        child1 component
        <div>{{foot}}</div>
    </div>
</template>
<script>
export default {
    inject:["foot"],
    mounted(){
        this.$parent.$on("child2ToChild1",()=>{
            console.log("child1 被触发");
        });
        console.log(this.$attrs);
    },
    methods:{
        eat(){
            console.log("回家吃饭...");
        },

    }
}
</script>
<style scoped>

</style>