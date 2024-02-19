<template>
  <div class="home">Home
    <p>My name is {{  name }} and my age is {{ age }}</p>
    <button @click="handleclick"> click me</button>
    <button @click="age++"> add 1 to age</button>
    <input type="text" v-model="name">
  </div>
</template>
<script>
import { ref } from 'vue'

export default {
  name: 'HomeView',
  setup(){

    let name=ref('mario')
    let age=ref(30)

    const handleclick = () =>{
      name.value='luigi'
      age.value=35
    }
    return{
      name,age,handleclick
    }
  },
  data(){
    return {
      score:5
    }
  }
} 
</script>
