<script setup>
import { ref } from 'vue';

</script>
<template>
    <slot name="top">
        <h4>Contenido por defecto de slot</h4>
    </slot>
    
    <div class="child">
        <h2>Este es un componente hijo</h2>
    </div>
    <slot name="bottom">
        <h4>Contenido por defecto de slot</h4>
    </slot>
</template>
<style>
.child {
    border: 5px solid black;
    padding: 10px;
    margin: 10px;
}
</style>