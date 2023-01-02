<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import NavbarVue from './components/Navbar.vue';
import { gsap } from 'gsap';
import { onMounted } from 'vue';


onMounted(() => {
    const tl = gsap.timeline()
    tl.from('.home', {
        opacity:0,
        delay:1.2,
        // y:400,
        ease:"power3.inOut"
    },"<0.1")
})

</script>

<template>
  <div class="home">
    <RouterView />
  </div>
 
</template>

<style scoped>

</style>
