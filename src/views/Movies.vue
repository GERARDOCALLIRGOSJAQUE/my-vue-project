<script setup>
import { ref } from "vue";
import HeaderComponent from "../components/HeaderComponent.vue";

const movies = ref([
    {title: "Harry Potter", duration: "2h 32m", director: "Chris Columbus"},
    {title: "The lord of the Rigns", duration: "3h 21m", director: "Peter Jackson"},
    {title: "Interstellar", duration: "2h 49m", director: "Christopher Nolan"}
])
</script>
<template>
    <HeaderComponent />
    <div>
        <h1>Movies</h1>
        <ul>
            <li v-for="movie in movies" :key="movie.title" class="movie">
                <h2>{{movie.title}}</h2>
                <p>Duration: {{ movie.duration }}</p>
                <p>Director: {{ movie.director }}</p>
            </li>
        </ul>
    </div>
</template>
<style>
.movie {
    border: 1px solid #ccc;
    padding: 10px;
    margin-bottom: 10px;
}
</style>