<template>
  
</template>

<script setup>
import {onUpdated} from "vue"
    const props = defineProps(["dataProps"])
onUpdated(()=>{
    alert("Giá trị của biến age đã thay đổi")
})
</script>

<style>

</style>