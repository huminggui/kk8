<template>
    <div>
        <input :type="type" :value="value" @input="onInput" />
    </div>
</template>
<script>
export default {
    props:{
        type:{
            type:String,
            default:""
        },
        value:{
            type:String,
            default:"默认值"
        }
    },
    data(){
        return {

    }},
    methods:{
        onInput(e){
            this.$emit("input",e.target.value);
        }
    }
}
</script>
<style>

</style>