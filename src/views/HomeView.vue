<template>
  <div class="home">
    <h1>Home</h1>
    <input type="text" v-model="search">
    <p>search term - {{ search }}</p>
    <div v-for="name in matchingNames" :key="name">{{ name }}</div>

    <button @click="handleClick">Stop watching</button>
  </div>
</template>
<script>
import { computed, ref, watch, watchEffect } from 'vue'

export default {
  name: 'HomeView',
  setup(){
    const search=ref('')
    const names=ref(['mario','yoshi','luigi','toad'])

    const stopwatch=watch(search,()=>{
      console.log('watch function run')
    })
    const stopwatchEffect=watchEffect(()=>{
      console.log('watch effect function run',search.value)

    })
    const matchingNames=computed(()=>{
      return names.value.filter((name)=> name.includes(search.value))
    })
    const handleClick=()=>{
      stopwatch()
      stopwatchEffect()
    }
    return{names,search,matchingNames,handleClick}
  }
} 
</script>
