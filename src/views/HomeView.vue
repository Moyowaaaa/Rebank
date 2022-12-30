<script setup lang="ts">
import Navbar from '../components/Navbar.vue'
import TitleSection from '../components/TitleSection.vue'
import AboutSection from '../components/AboutSection.vue'
import Jumbotron from '../components/JumbtronPostor.vue'
import Faqs from '../components/FaqsSection.vue'
import GetStartedSection from '@/components/GetStartedSection.vue'
import Main from '../layouts/Main.vue'
</script>

<template>
<div>
<!-- <Navbar /> -->
<Main>
    <TitleSection />
<AboutSection />
 <Jumbotron />
<Faqs />
<GetStartedSection /> 
</Main>

</div>
</template>
