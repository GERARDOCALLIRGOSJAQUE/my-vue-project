<script setup>
import HeaderComponent from './components/HeaderComponent.vue';
import { ref } from 'vue';
  //let number = 0;//variable no reactiva
  let number = ref(0);//variable reactiva
  /*setInterval(() => {
    number.value++;
  }, 1000);*/
  const addOne = () => {
    number.value++;
  };
  
</script>

<template>
  <HeaderComponent></HeaderComponent>
  <h1 class="title">Hola a todos!</h1>
  <h2 @click="addOne">Contador {{ number }}</h2>
</template>

<style scoped>
  .title {
    background-color: blue;
    color: red;
  }
</style>