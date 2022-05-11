<template>
 
  <TestStore/>
  <CountButton/>
</template>

<script lang="ts">
import useUrlAxios from './hooks/useUrlAxios'
import TestStore from "./components/TestStore.vue"
import CountButton from "./components/CountButton.vue"

export default ({
  name: 'App',
  components:{TestStore,CountButton},
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
.wrap{
  width:400px;
  height:400px;
  background-color:grey;
   position: fixed;
  left: 50%;
  top: 50%;
  margin-left: -200px;
  margin-top: -200px;
}
</style>
