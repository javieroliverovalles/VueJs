<!-- eslint-disable vue/valid-v-for -->
<!-- eslint-disable vue/valid-template-root -->
<template>
<div>
    <h2>Lista de tareas</h2>
    <input type="text" v-model="nuevaTarea" @keyup.enter="addTarea" >
    <ul>
        <li v-for="tarea in tareas" :key="index">
            {{ tarea }}
            <button @click="deleteTarea">Borrar tarea</button>
        </li>
    </ul>
</div>
</template>

<script setup>
import { ref } from 'vue';
const tareas = ref([]);
const nuevaTarea = ref('');

const addTarea = () => {
tareas.value.push(nuevaTarea.value);
nuevaTarea.value = '';
}

const deleteTarea = (index) => {
    tareas.value.splice(index,1);
}
</script>

<style scoped></style>