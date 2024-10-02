<template>
<div>
    <h1>Count: {{count}}</h1>
    <button @click="increaseCount">Counter</button>
  </div>
</template>

<script setup>
    import {ref, onUpdated,onBeforeUpdate} from "vue"
    const count = ref(0)
    function increaseCount(){
        count.value++
    }
    onUpdated(()=>{
        console.log("Dữ liệu đã thay đổi");
    })
</script>

<style>

</style>