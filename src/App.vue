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
  
  const myValue = ref('patata');
  let myCondition = true;
</script>

<template>
  <HeaderComponent></HeaderComponent>
  <h1>{{ myValue}}</h1> <!--v-bind:id="myId" = :id="myId"-->
  <input type="text" v-model="myValue"> <!--v-bindcrear reactividad"-->
  <h2 @click="addOne">Contador {{ number }}</h2>
  <h1 :class="myCondition ? 'title' : 'black'">Clase dinamica</h1>
  <h1 :class="{title: myCondition, black: true}">Clase dinamica</h1>
</template>

<style scoped>
  .title {
    background-color: blue;
    color: red;
  }
  .black {
    color: rgb(0, 0, 0);
  }
</style>