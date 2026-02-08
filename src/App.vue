<script setup>
import HeaderComponent from './components/HeaderComponent.vue';
import { ref } from 'vue';
import ChildComponent from './components/ChildComponent.vue';

  const text = "Info desde variable padre";
  const person = {
    sex: "hombre",
    age: 30
  }
</script>

<template>
  <h1>Renderizado de lista | v-for</h1>
  <ChildComponent :msg="text" :person="person"></ChildComponent>
  <ChildComponent msg="Otro mensaje" ></ChildComponent>
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