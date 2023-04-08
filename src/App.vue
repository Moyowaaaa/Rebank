<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import NavbarVue from './components/Navbar.vue';
import { gsap } from 'gsap';
import { onMounted } from 'vue';
import LocomotiveScroll from "locomotive-scroll";


</script>

<template>
  <div class="home">
    <RouterView />
  </div>
 
</template>

<style scoped>

</style>
