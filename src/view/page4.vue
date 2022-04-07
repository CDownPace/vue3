<template>
  <div>
<div>{{ nowTime }}</div>
<div><button @click="getNowTime">显示时间</button></div>
  </div>
</template>
<script lang="ts">
import {nowTime,getNowTime} from './hooks/useNowTime'
const app = {
  name: "App",
  setup() {
    return{
      nowTime,getNowTime,
    }
  },
};
export default app;
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