<!-- eslint-disable vue/multi-word-component-names -->
<template>
<div class="sidebar">
    <div>
        <h2>Barra lateral</h2>
        <ul>
            <li class="lista-sin-puntos"><RouterLink to="/contador">Contador</RouterLink></li>
            <li class="lista-sin-puntos"><RouterLink to="/lista-de-tareas">Lista de tareas</RouterLink></li>
        </ul>
    </div>
</div>
</template>

<script setup>
</script>

<style scoped>
.sidebar{
    width: 250px;
    background-color: #f0f0f0;
    padding: 20px;
    display: flex;
    min-height: 100vh;
}
.lista-sin-puntos {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
</style>