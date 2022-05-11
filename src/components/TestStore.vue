<template>
<h2 class="">
{{store.helloWorld}}
{{store.count}}
</h2>
</template>
<script lang="ts" setup>
import {mainStore} from "../store/index"
const store = mainStore();
</script>