<template>
    <h1>This is a component thing.</h1>
    <button @click="$emit('buttonClicked')">{{ text }}</button>
</template>

<!--With Script setup-->
<script setup lang="ts">

const props=defineProps({
    text:{
        type:String,
        default:"No Props are passed"  
    }
    })
const emit=defineEmits(['buttonClicked'])
</script>


<!--Without Script setup
<script>
    import {ref} from "vue"

    export default{
        props:{
            text:{
                type:String,
                default:"No Props are passed"
            }
        },
        emits:['buttonClicked']
    }
</script>-->