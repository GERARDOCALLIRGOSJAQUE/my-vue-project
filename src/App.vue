<script setup>
import HeaderComponent from './components/HeaderComponent.vue';
import { ref } from 'vue';
  const movies = ["Lord of the Rings", "Harry Potter", "Star Wars"];
const animals = [
    {
        id: 1,
        name: 'León',
        img: 'https://via.placeholder.com/150'
    },
    {
        id: 2,
        name: 'Tigre',
        img: 'https://via.placeholder.com/150'
    },
    {
        id: 3,
        name: 'Elefante',
        img: 'https://via.placeholder.com/150'
    }
]

</script>

<template>
  <h1>Renderizado de lista | v-for</h1>
  <div>
    V-for index
    <p v-for="(movie, index) in movies" :key="movie">
      {{ index + 1 }} - {{ movie }}
    </p>
    <ul>
      <li v-for="animal in animals" :key="animal.id">
        {{ animal.name }}
        <img :src="animal.img" width="200px"/>
      </li>
    </ul>
  </div>
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