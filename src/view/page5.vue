<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>
     <h2>你好</h2>
    <h2>请选择你最喜欢的城市</h2>
    <button v-for="(item,index) in data.city" :key="index" @click="data.selectCityFun(index)">
      {{index}}:{{item}}
    </button>
    <div>你最喜欢的城市是:{{data.selectCity}}</div>
    <div> <button @click="data.overAction()">点餐完毕</button></div>
    <div>{{data.overText}}</div>
  </div>
</template>

<script lang="ts">
import { ref,reactive,watch } from 'vue';

export default ({
  name: 'App',
  setup(){
    const data=reactive({
      city:['北京','上海','广州'],
      selectCity:'',
      overText:'红浪漫',
      selectCityFun:(index:number)=>{
        data.selectCity=data.city[index];
      },
      overAction:()=>{
        data.overText+='点餐完成|'
        // document.title=data.overText
      }
    });

    watch([()=>data.overText,()=>data.selectCity],(newValue,oldValue)=>{
      console.log('111'+newValue)
      console.log('222'+oldValue)
    })
    return {
      data,
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
