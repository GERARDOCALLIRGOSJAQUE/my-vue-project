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
  const myId = 'patata';
  const myValue = ref('patata');
</script>

<template>
  <HeaderComponent></HeaderComponent>
  <h1 :id="myId">Hola a todos!</h1> <!--v-bind:id="myId" = :id="myId"-->
  <input type="text" :value="myValue"> <!--v-bindcrear reactividad"-->
  <h2 @click="addOne">Contador {{ number }}</h2>
</template>

<style scoped>
  .title {
    background-color: blue;
    color: red;
  }
</style>