<template>
  <h2>Chiều rộng cửa sổ: {{ widthWindow }}</h2>
</template>

<script setup>
import { ref, onMounted, onUnmounted } from 'vue'

const widthWindow = ref(0)

const updateWidth = () => {
  widthWindow.value = window.innerWidth
}

onMounted(() => {
  widthWindow.value = window.innerWidth
  window.addEventListener('resize', updateWidth)
})

onUnmounted(() => {
  window.removeEventListener('resize', updateWidth)
})
</script>

<style>

</style>
