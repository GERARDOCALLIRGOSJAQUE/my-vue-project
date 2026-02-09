<script setup>
import { ref, watch, watchEffect } from "vue";

//const userName = ref({name: "Adrián"});
const userName = ref("Adrián");
const setName = () => { 
  userName.value = "Maria";
  };

  /*watch(userName, 
  (newValue, oldValue) => {
    console.log("User name modified");
  }, {
    immediate: true,
    deep: true
  })*/
 watchEffect(() => {
    console.log("User name modified to: ", userName.value);
  })
</script>

<template>
  <h1>Watch | Vigilancia de cambios</h1>
  <h2>Hola {{ userName }}</h2>
  <input type="text" v-model="userName">
  <button @click="setName">Cambiar nombre</button>
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