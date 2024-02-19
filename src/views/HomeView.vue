<template>
  <div class="home">
    <h1>Home</h1>
    <h2>Refs</h2>
    <p>{{  One.name }} - {{ One.age }}</p>
    <button @click="updateOne"> Update first one</button>
    <h2>Reactive</h2>
    <p>{{ Two.name }} - {{ Two.age }}</p>
    <button @click="updateTwo"> Update second one</button>

  </div>
</template>
<script>
import { ref ,reactive} from 'vue'

export default {
  name: 'HomeView',
  setup(){

   const One=ref({name:'mario',age:30})
   const Two=reactive({name:'luigi',age:35})

   const updateOne=()=>{
    One.value.age= 40
   }
   const updateTwo=()=>{
    Two.age= 45
   }
    return{
      One,updateOne,Two,updateTwo
    }
  },

} 
</script>
