<script setup lang="ts">

import { gsap } from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';
import { onMounted } from 'vue';
gsap.registerPlugin(ScrollTrigger)


onMounted(() => {
    

   let posterTl = gsap.timeline({
    scrollTrigger:{
        trigger:'.jumbotron',
        start: 'top center',
    end: () => window.innerHeight/45 + 'top',
      
        scrub:0.1
    }
   })

// posterTl.from('.jumbotron',{
//     duration:2,
//     ease:"power3.inOut",
//     backgroundAttachment:"scroll",
//     backgroundPositionY:"40vh, 40vh",
//     opacity:0,
// })
   posterTl.from('.jumboText',{opacity:0,duration:0.8, ease:"power2.inOut"})
   posterTl.fromTo(['.jumboText','.scribble'],{opacity:0},{ y: 0, opacity: 1, duration:1.5, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)" },'<0.1');
   posterTl.from('.jumbotronButton', {duration:1.5,scale:2.5,opacity:0, ease:"power3.inOut"})
   posterTl.from('.jumboHero', {opacity:0, ease:"power3.inOut", duration:1.2, y:200},"<0.1")
    
})
</script>


<template>
    <div class="jumbotron w-screen lg:w-full h-screen bg-black text-white  flex flex-col items-center justify-center">

        <div class="w-11/12 lg:w-7/12 flex flex-col py-4 gap-4 lg:items-center">
            <div class="w-full flex justify-start">
                <p class="jumbotext font-[roboto-medium]">Personalisation</p>
            </div>
            <h1 class="jumboText flex text-center text-3xl lg:text-5xl font-[grotesk-bold] z-20">Stand out from the crowd with a card <br/> and app to match your style</h1>
            <div class="scribble relative left-32 lg:left-64 bottom-10 w-max">
                <img src="../assets/images/scribble.svg" />
            </div>
            <p class="jumboHero text-center font-[roboto] text-sm lg:text-base">
                Don’t blend into the crowd with a boring bank card, stand out! Choose a card colour to suit your style <br/> and the app will change to match.
            </p>

            <div class="w-full flex justify-center">
                <button class="jumbotronButton flex border-2 border-white rounded py-4 px-8 font-[roboto] text-sm lg:text-base">
                    Find out more
                </button>
            </div>
        </div>
    </div>
</template>


<style scoped>
.jumbotron{
    overflow-x: hidden;
    background-image: url('../assets/images/jumbotronLeft.svg'), url('../assets/images/jumbotronRight.svg');
    background-repeat:  no-repeat;
    background-size: contain contain;
  
    background-position-y: bottom, bottom;
    background-position-x:left,right ;
    background-attachment: fixed, fixed;
}

@media screen and (max-width:485px) {
    .jumbotron{
        background-size: cover;
    }
}
</style>