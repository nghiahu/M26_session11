<template>
  <div>
    <h1>Ứng dụng đếm số:</h1>
    <div>Count: {{timer}}</div>
  </div>
</template>

<script setup>
    import {onMounted,ref} from "vue"
    const timer =  ref(0)
    onMounted(()=> {
    setInterval(()=>{
            timer.value++
        },1000)
    })
</script>

<style>

</style>