<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
     <h2>你好</h2>
    <h2>请选择你最喜欢的城市</h2>
    <div v-if="loading">Loading...</div>
   <img v-if="loaded" :src="result.imgUrl"/>
  </div>
</template>

<script lang="ts">
import useUrlAxios from '../hooks/useUrlAxios'

export default ({
  name: 'App',
  setup(){ 
    const {result,loading,loaded}= useUrlAxios("https://apiblog.jspang.com/default/getGirl")
    return {result,loading,loaded}

  },
  

});

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
