<script setup>
import HeaderComponent from './components/HeaderComponent.vue';
import { ref } from 'vue';
import ChildComponent from './components/ChildComponent.vue';
const displayName = ref('');
const setName = (name) => {
  displayName.value = name;
};

</script>

<template>
  <h1>Renderizado de lista | v-for</h1>
  <h2>Hola {{ displayName }}</h2>
  <ChildComponent @login="setName" ></ChildComponent>
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