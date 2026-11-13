<!-- eslint-disable vue/multi-word-component-names -->
<template>
    <div>
        <h4>La temperatura actual es: {{ weatherStore.temperatura }} °</h4>
    </div>
</template>
<script setup>
import { useWeather } from '@/composables/useWeather';
import { onMounted } from 'vue';
import { useWeatherStore } from '@/stores/weatherStore';

const weatherStore = useWeatherStore();

onMounted(() => {
    useWeather();
})
</script>
<style scoped></style>