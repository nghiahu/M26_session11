<template>
  <div>
    <button @click="handleisShow">Toggle</button>
    <Exercise05ChildrenVue v-if="isShow"/>
  </div>
</template>

<script setup>
    import {ref} from "vue"
    import Exercise05ChildrenVue from "./Exercise05Children.vue";
    const isShow = ref(false)
    const handleisShow=()=>{
        isShow.value = !isShow.value
    }

</script>

<style>

</style>