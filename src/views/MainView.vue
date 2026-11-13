<template>
<Header></Header>
<div class="container">
    <Sidebar></Sidebar>
    <div class="content">
        <RouterView></RouterView>
    </div>
</div>
</template>

<script setup>
import Sidebar from '@/components/Sidebar.vue';
import Header from '@/components/Header.vue';
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