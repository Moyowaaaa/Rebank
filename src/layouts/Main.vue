<template>
    <Navbar/>
    <div class="flex flex-col w-full items-center">

    
    <slot />
</div>
</template>

<script setup lang="ts">
import Navbar from '../components/Navbar.vue' 
</script>

<style scoped>

</style>