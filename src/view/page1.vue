<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
    <h2>你好</h2>
    <h2>请选择你最喜欢的城市</h2>
    <button v-for="(item,index) in girls" :key="index" @click="selectGirlFun(index)">
      {{index}}:{{item}}
    </button>
    <div>你最喜欢的城市是:{{selectGirl}}</div>
  </div>
</template>

<script lang="ts">
import { defineComponent,ref } from 'vue';

export default defineComponent({
  name: 'App',
  setup(){
    const girls =ref(["北京","广州","杭州"])
    const selectGirl=ref("")
    const selectGirlFun=(index:number)=>{
      selectGirl.value=girls.value[index];
    }  
    return {
    girls,
    selectGirl,
    selectGirlFun,
  }
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
