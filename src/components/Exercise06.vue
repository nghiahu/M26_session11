<template>
  <div>
    <h3>count: {{count}}</h3>
    <button @click="increaseCount">Increment</button>
  </div>
</template>

<script setup>
import {ref,onUpdated} from "vue"
    const count = ref(0)
    function increaseCount(){
        count.value++
    }
    onUpdated(()=>{
        document.title = count.value
    })
</script>

<style>

</style>