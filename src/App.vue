<script setup>
import { computed, ref } from 'vue';
import ChildComponent from './components/ChildComponent.vue';
const userName = ref('Juan');
const nameLength = computed(() => {
  return userName.value.length;
});

</script>

<template>
  <h1>Computed | Propiedades computadas</h1><!--Son una forma de transferir info de un padre aun hijo -->
  <input type="text" v-model="userName">
  <h2>Hola {{ userName }}</h2>
  <h3>Tu nombre tiene {{ nameLength }} letras</h3>
  
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