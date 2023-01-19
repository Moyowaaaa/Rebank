<script setup lang="ts">
import Navbar from '../components/Navbar.vue'
import TitleSection from '../components/TitleSection.vue'
import AboutSection from '../components/AboutSection.vue'
import Jumbotron from '../components/JumbtronPostor.vue'
import Faqs from '../components/FaqsSection.vue'
import GetStartedSection from '@/components/GetStartedSection.vue'
import Main from '../layouts/Main.vue'
import { ref,onMounted } from 'vue'
import mainImage from '../assets/images/titleSectionMain.svg'
import shortBar from '../assets/images/lineShort.svg'
import mediumBar from '../assets/images/lineMedium.svg'
import TallBar from '../assets/images/lineTall.svg'
import colorGroup from '../assets/images/titleColorGroup.svg'
import groteskFont from '../assets/fonts/SpaceGrotesk-Bold.otf'

const assetsLoaded = ref<boolean>(false)

const assets = ref([
    mainImage,shortBar,mediumBar,colorGroup,TallBar
])


onMounted(() => {
    const promises:any[] = []
    assets.value.forEach(asset => {
        const img = new Image()
        img.src = asset
        promises.push(new Promise((resolve, reject) => {
          img.onload = resolve
          img.onerror = reject
        }))        
    })
    new Promise((resolve,reject) => {
            const font = new FontFace('grotesk-bold',`url(${groteskFont})`);
            font.load().then(resolve,reject)
        })
        
    Promise.all(promises).then(() => {
        assetsLoaded.value = true
      })
})

// onMounted(() => {
//     const assets = [
//         // new Promise((resolve,reject) => {
//         //     const image = new Image();
//         //     // image.onload = resolve
//         //     // image.onerror = reject;
//         //     // image.src = mainImage
//         // }),
//         new Promise((resolve,reject) => {
//             const font = new FontFace('grotesk-bold','url(../assets/fonts/SpaceGrotesk-Bold.otf)');
//             font.load().then(resolve,reject)
//         })
//     ]
//     Promise.all(assets) 
//     .then(() => {
//         assetsLoaded.value = true
//     }).catch((error) => {
//         console.log(error)
//     })
// })
  


</script>

<template>
<div v-if="assetsLoaded">
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


