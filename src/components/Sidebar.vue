<!-- eslint-disable vue/multi-word-component-names -->
<template>
<div class="sidebar">
    <div>
        <h2>Bienvenido</h2>
        <h3>Nombre: {{ nombre }}</h3>
        <h3>Email:{{ email }}</h3>
        <ul>
            <li class="lista-sin-puntos"><RouterLink to="/contador">Contador</RouterLink></li>
            <li class="lista-sin-puntos"><RouterLink to="/lista-de-tareas">Lista de tareas</RouterLink></li>
            <li class="lista-sin-puntos"><RouterLink to="/registrar">Registar</RouterLink></li>
        </ul>
    </div>
</div>
</template>

<script setup>
import { useRegistrarStore } from '@/modules/registro/stores/registrarStore';
import { ref, watch } from 'vue';
const registrarStore = useRegistrarStore();
const nombre = ref(registrarStore.nombre.value);
const email = ref(registrarStore.email.value);
watch(() => registrarStore.nombre, (newValue) => {
    nombre.value = newValue;
});
watch(() => registrarStore.email, (newValue) => {
    email.value = newValue;
});
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