<script setup></script>
<template>
    <header class="header">
        <h1>Movies</h1>
        <nav>
            <ul class="nav-list">
                <li><router-link to="/">Home</router-link></li>
                <li><router-link to="/movies">Movies</router-link></li>
                <li><router-link :to="{name: 'create'}">Create</router-link></li>
            </ul>
        </nav>
    </header>
</template>
<style>
.header {
    background-color: #333;
    color: white;
    padding: 10px;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
.nav-list {
    list-style: none;
    display: flex;
    gap: 10px;
}
</style>