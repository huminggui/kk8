<template>
    <div>
        child2 component {{name}}
        <button @click="emitChild2">点击组件2传值组件1</button>
        <!--卡槽传输数据给父类使用的这个卡槽。数据在这个作用域范围类是可以使用的
        所以叫做作用域卡槽
        -->
        <slot name="childSlot" :d="slotData" :c="c"></slot>
        <div>
            <input type="text" />
        </div>
        
        {{v}}
    </div>
</template>
<script>
export default {
    data(){
        return{
            slotData:"我是child2的数据",
            c:"cccccc",
            v:"ha"
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