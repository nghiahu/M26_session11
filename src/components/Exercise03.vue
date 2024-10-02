<template>
  <div>
    <div>Current Company: {{ CurrentCompany }}</div>
    <div>Age: {{ age }}</div>
    <button @click="randomNumber">Random</button>
    <br>
    Bài 4 <br>
    <button @click="increaseAge">increase Age</button>
    <div>Age: {{age2}}</div>
    <Exercise04Vue :dataProps="age2 "/>
  </div>
</template>

<script setup>
import { ref, onMounted, onBeforeMount } from "vue";
import Exercise04Vue from "./Exercise04.vue";
const age = ref(1);
const age2 = ref(1);
const array = ["Rikkei Academy", "Rikkei Education", "Rikkei Fukuoka"];
const CurrentCompany = ref("");

onBeforeMount(() => {
  CurrentCompany.value = "Rikkei Academy";
});

function randomNumber() {
  age.value = Math.floor(Math.random() * 10) + 1;

  if (age.value === 1 || age.value === 4 || age.value === 7 || age.value === 10) {
    CurrentCompany.value = array[0];
  } else if (age.value === 2 || age.value === 5 || age.value === 8) {
    CurrentCompany.value = array[1];
  } else {
    CurrentCompany.value = array[2];
  }
}
function increaseAge(){
    age2.value++
}
</script>

<style>
</style>
