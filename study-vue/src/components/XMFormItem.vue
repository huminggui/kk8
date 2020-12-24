<template>
    <div>
        <label v-if="label">{{label}}</label>
        <slot></slot>
        <p v-if="error">{{error}}</p>
    </div>
</template>
<script>
import XMInput from "./XMInput"
export default {
    props:{
        error:{
            type:String,
            default:""
        },
        label:{
            type:String,
            default:""
        }
    },
    data(){
        return {

        }
    },
    components:{
        XMInput
    }
 
}
</script>
<style scoped>

</style>