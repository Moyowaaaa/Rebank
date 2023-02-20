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
import groteskMedium from '../assets/fonts/SpaceGrotesk-Medium.otf'
import groteskRegular from '../assets/fonts/SpaceGrotesk-Regular.otf'

import Lenis from '@studio-freight/lenis'

// useLocomotiveScroll('#container')

const smoothScroll = ()=>{
  const lenis = new Lenis({
  duration: 1.2,
  easing: (t) => Math.min(1, 1.001 - Math.pow(2, -10 * t)), // https://www.desmos.com/calculator/brs54l4xou
  direction: 'vertical', // vertical, horizontal
  gestureDirection: 'vertical', // vertical, horizontal, both
  smooth: true,
  mouseMultiplier: 1,
  smoothTouch: false,
  touchMultiplier: 2,
  infinite: false,
})

function raf(time:any) {
  lenis.raf(time)
  requestAnimationFrame(raf)
}

requestAnimationFrame(raf)
}




const assetsLoaded = ref<boolean>(false)

const assets = ref([
    mainImage,shortBar,mediumBar,colorGroup,TallBar
])


onMounted(() => {
    smoothScroll()
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
            const font2 = new FontFace('grotesk-medium',`url(${groteskMedium})`);
            font.load().then(resolve,reject)
            const font3 = new FontFace('grotesk',`url(${groteskRegular})`);
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
<div v-if="assetsLoaded" ref="container"  id="container">
<!-- <Navbar /> -->
<Main >
    

    <TitleSection />
<AboutSection />
 <Jumbotron />
<Faqs />

<GetStartedSection /> 
</Main>

</div>
</template>


