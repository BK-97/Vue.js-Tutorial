<template>
  <div class="home">Home
    <p>My name is {{  name }} and my age is {{ age }}</p>
    <button @click="handleclick"> click me</button>
  </div>
</template>
<script>

export default {
  name: 'HomeView',
  setup(){
    let name='mario'
    let age=30

    const handleclick = () =>{
      console.log('you clicked me')
    }
    return{
      name,age,handleclick
    }
  }
} 
</script>
