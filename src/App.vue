<template>
<SingupForm />
</template>

<script>

import SingupForm from './components/SingupForm.vue';
export default {
  name: 'App',
  components:{SingupForm},
  
}

</script>

<style>
#app, .modals,#modalsid {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #444;
  margin-top: 60px;
}
body{
  margin: 0;
  background: #eee;
}

</style>
