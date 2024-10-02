<template>
  <input type=" text" v-model="inputValueTitle">
</template>

<script setup>
    import {ref,onUpdated} from "vue"
    const inputValueTitle = ref("")
    onUpdated(()=>{
        document.title = inputValueTitle.value
    })
</script>

<style>

</style>