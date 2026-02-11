<script setup>
import { reactive, ref, watch, watchEffect } from "vue";

const movie = reactive({
  title: "",
  duration: 0,
  director: ""
})
const handleSubmit = () => {
  if(!movie.title || !movie.duration || !movie.director) {
    alert("Please fill in all fields");
    return;
  }
  console.log(movie);
}
</script>

<template>
  <h1>Forms</h1>
  <form @submit.prevent="handleSubmit" class="form">
    <label for="title">Title</label>
    <input type="text" id="title" v-model="movie.title">

    <label for="duration">Duration</label>
    <input type="number" id="duration" v-model = "movie.duration">

    <label for="director">Director</label>
    <input type="text" id="director" v-model = "movie.director">
    <button>Submit</button>
  </form>
</template>

<style scoped>
  .form {
    display: flex;
    flex-direction: column;
    gap: 1rem;

  }
  .title {
    background-color: blue;
    color: red;
  }
  .black {
    color: rgb(0, 0, 0);
  }
</style>