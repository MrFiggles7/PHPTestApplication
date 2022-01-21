<template>
  <div id="app">
    {{thing}}
  </div>
</template>

<script>


export default {
  name: 'App',

  data() {
    return{
      thing: 'this thing'
    }
  },

  created() {
    const axios = require('axios');

    axios.get('http://localhost/PHPTestApplication/api/actor/read.php').then((response)=>{
      this.thing = response
    })
  },

  components: {

  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
