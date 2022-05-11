<template>
  <h2 class="">
  <button @click="handleClick">点击增加</button>
  <button @click="handleClickAction">修改数据($patch)</button>
  </h2>
</template>

<script lang="ts" setup>
import { mainStore } from "../store/index";
const store = mainStore();
// 第一种
const handleClick=()=>{
    store.count++
}
// 第二种
// const handleClickPatch=()=>{
//     store.$patch({
//         count:store.count+2,
//         helloWorld:store.helloWorld==='HelloDalian'?'HelloWorld':'HelloDalian'
//     })
// }
// 第三种
const handleClickPatch=()=>{
    store.$patch((state)=>{
        state.count++;
        state.helloWorld=state.helloWorld==='HelloDalian'?'HelloWorld':'HelloDalian'
    })
}

// 第四种
const handleClickAction=()=>{
    store.changeState()
}
</script>

<style lang="scss" scoped></style>