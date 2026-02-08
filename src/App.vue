<script setup>
import ChildComponent from './components/ChildComponent.vue';

</script>

<template>
  <h1>Slots</h1><!--Son una forma de transferir info de un padre aun hijo -->
  <h2>Este es el componente padre</h2>
  <ChildComponent>
    <template v-slot:top>
      <h3>Contenido desde el componente padre como slot</h3>
    </template>
    
  </ChildComponent>
  <ChildComponent>
    <template v-slot:bottom>
      <p>Lorem ips</p>
      <p>jnded iedie euded o</p>
    </template>
    
  </ChildComponent>
  
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