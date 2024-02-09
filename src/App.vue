<template>
  <div>
    <h1>This is {{ course }} project.</h1>
    <button @click="change">Click me!</button>
    <MyThing @buttonClicked="showAlert" text="This are props that are passed"/>
  </div>
  
</template>


<!--With Script setup-->
<script setup lang="ts">
  import { ref } from "vue";
  import MyThing from "@/components/MyThing.vue"

  const course = ref("VUE JS")

  const change=()=>{
    course.value="Mantra"
  }

  const showAlert=()=>{
    alert("Button is Clicked from the Component")
  }
</script>

<!--Without Script setup
<script>
  import {ref} from "vue";
  import MyThing from "@/components/MyThing.vue"

  export default {
    setup(){
      const course=ref("LOKESH")

      const change=()=>{
        course.value="Mantra"
      }

      const showAlert=()=>{
        alert("Button is Clicked from the Component")
      }

      return{
        course,
        change,
        showAlert
      }
    },
    components:{
      MyThing
    }
  }
</script>-->

<style>
button {
  padding: 10px 20px;
  font-size: 16px;
  background-color: #3498db;
  color: #ffffff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
}
</style>