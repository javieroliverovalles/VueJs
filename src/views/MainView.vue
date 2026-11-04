<template>
<div class="container">
    <Sidebar></Sidebar>
    <div class="content">
        <RouterView></RouterView>
    </div>
</div>
</template>

<script setup>
import Sidebar from '@/components/Sidebar.vue';
</script>

<style scoped>
.container {
    display: flex;
}
.content{
    padding: 20px;
    flex: 1;
}
</style>