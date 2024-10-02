<template>
  <h1>Exercise05Children</h1>
</template>

<script setup>
    import {ref,onBeforeUnmount,onUnmounted} from "vue"
    onBeforeUnmount(()=>{
    console.log("Component is about to be unmounted");
    })
    onUnmounted(()=>{
        console.log("Component has been unmounted");
    })
</script>

<style>

</style>