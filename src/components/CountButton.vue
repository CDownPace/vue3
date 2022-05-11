<template>
  <h2 class="">
  <button @click="handleClick">点击增加</button>
  </h2>
</template>

<script lang="ts" setup>
import { mainStore } from "../store/index";
const store = mainStore();
const handleClick=()=>{
    store.count++
}
</script>

<style lang="scss" scoped></style>