<template>
    <div>
        child1 component
    </div>
</template>
<script>
export default {
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