<template>
    <div class="about w-full h-auto  flex flex-col gap-4 ">

        <div class="about-section  min-h-screen">
            <h1 class="lg:pl-10 font-[grotesk-bold] text-lg py-6 px-2  text-start">
        Used by the world's most amazing companies
    </h1>
        <MarqueeVue />

        <div class="hidden lg:flex absolute  w-[10rem] object-cover right-0 mt-6" >
            <img src="../assets/images/showcaseColorGroup.svg" class="w-full"/>
        </div>


        <div class="w-screen lg:w-full lg:mt-[8rem]  flex flex-col lg:flex-row gap-6 ">
            <div class="w-[10rem] mx-auto lg:mx-0 lg:w-7/12 ">
                <div class="showcase flex my-32 justify-center lg:justify-start">
            <img src="../assets/images/showcaseOrange.svg" />
            <img src="../assets/images/showCaseYellow.svg" />
        </div>


        <div class="lg:relative bottom-[56rem] hidden lg:flex flex-col  h-[5rem] w-max justify-between left-[28rem] gap-32">
            <img src="../assets/images/showcaseBlue.svg" class="showcaseBlue"/>
            <img src="../assets/images/showcasePink.svg"  class="showcasePink"/>
        </div>

        <div class="-z-50 lg:relative bottom-[29.5rem] hidden lg:flex flex-col  h-[5rem] w-max justify-between left-[25rem] ">
            <img src="../assets/images/Ellipse1.svg" class="w-[5.2rem] lg:relative left-[13rem] bottom-[15rem]"/>

            <div class="flex flex-col items-center">
                <img src="../assets/images/Ellipse2.svg" class="lg:relative top-[8.5rem] w-[7rem]" />
                <img src="../assets/images/Ellipse3.svg" class="w-[10rem]"/>
            </div>
            
        </div>
            </div>


            <div class="w-full lg:w-7/12  flex flex-col lg:justify-end mb-64">
                <div class="about-hero flex flex-col gap-4">
            <p class="font-[grotesk-medium]">Physical Card</p>
            <h1 class="text-4xl w-11/12 mx-auto lg:mx-0 lg:text-6xl font-[grotesk-bold] lg:w-[45rem]">Spend anywhere with a physical debit card</h1>
            <p class="text-lg w-11/12 mx-auto lg:mx-0 font-[grotesk] lg:w-[39rem] lg:text-justify">The debit card is designed to spend everywhere and everywhere with simplicity and transparency built in. An RFID transponder embedded in its core enables you to pay with a quick touch-free wave.</p>
      

            <button class=" w-11/12 mx-auto lg:mx-0 lg:w-max py-4 px-6 rounded border-2 border-black font-[grotesk]">Find out more</button>
        </div>
            </div>
        </div>


        </div>


        <div class="spending-section min-h-screen  w-full flex flex-col my-6 items-center mb-52">

            <div class="flex flex-col lg:flex-row gap-4   items-center w-full ">
                <div class="spendingHero w-full lg:w-6/12  flex flex-col lg:items-start lg:pl-4" >
                    <p class="font-[grotesk-medium]">Companion App</p>
                    <h1 class="text-4xl lg:text-6xl font-[grotesk-bold] w-screen w-11/12 mx-auto lg:mx-0 lg:w-[50rem] text-center lg:text-left">Spending insights at your</h1>
                    <div class="flex flex-col lg:flex-row gap-6 items-center lg:items-start">
                        <h1 class="text-4xl text-center lg:text-6xl font-[grotesk-bold]">fingertips</h1>
                        <div class="flex flex-col gap-4">
                            <p class="text-base font-[grotesk] pt-4 w-11/12 mx-auto lg:mx-0 lg:w-full ">Engineered for clarity and speed to take your everyday spending experience to the next level. Instant transfers, virtual cards and heads up displays helps give you piece of mind about your finances.</p>
                        
            <button class="w-11/12 mx-auto lg:mx-0 lg:w-max py-4 px-6 rounded border-2 border-black font-[grotesk]">Find out more</button>
                        </div>
                     
                    </div>
                    
                </div>


                <div class="w-[20rem]  lg:w-6/12  flex items-center lg:justify-center h-[50rem]">
                    <img src="../assets/images/scribble2.svg" class="hidden lg:flex lg:relative  lg:self-end lg:left-[6.5rem] lg:bottom-6"/>
                    <img src="../assets/images/spendingYellow.svg" class="Yellow relative lg:my-32 lg:right-32 right-[-4rem]"/>
                    <img src="../assets/images/spendingPink.svg" class="Pink relative lg:right-48 top-20 lg:top-12 right-[15rem]" />
                </div>
            </div>

        </div>
    



      
      
    </div>
</template>

<script setup lang="ts">
import MarqueeVue from './Marquee.vue';
import AboutImages from '../components/AboutImages.vue'
import { gsap } from 'gsap';
import ScrollTrigger from 'gsap/ScrollTrigger';
import { onMounted } from 'vue';
gsap.registerPlugin(ScrollTrigger)
 onMounted(() => {
    let spendingTl = gsap.timeline({
        scrollTrigger:{
            trigger:'.spending-section',
            start: 'top center',
            end:'top +=10',
        
            scrub:0.1
        }
    })

    spendingTl.from(['.Yellow','.Pink'],{
        opacity:0,
        duration:1.5,
        stagger:0.5,
        ease:"power3.inOut",
        y:400
    })

    spendingTl.fromTo('.spendingHero',  { opacity: 0,scaleX:0.8 },
    {
      y: 0,
      opacity: 1,
      duration: 1.5,
    //   clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)",
    scaleX: 1, 
    z: -500
    },"<0.1")


    let aboutTl = gsap.timeline({
        scrollTrigger:{
            trigger:'.about-section',
            start: 'top center',
            end:'top +=100',
    
            scrub:0.1
        }
    })


    aboutTl.from('.showcaseBlue',{
        scale:1.8,
        opacity:0,
        delay:0.5,
        ease:"power3.in"
    })
    aboutTl.from('.showcasePink',{
        scale:1.8,
        opacity:0,
        delay:0.5,
        ease:"power3.in"
    })

 })


</script>

<style scoped>


.about{
    max-width: 450rem;
 
    display: flex;
    flex-direction: column;
    align-items: center;
}


.about-section {
    background-image:
    /* url('../assets/images/Ellipse1.svg'),  */
    /* url('../assets/images/Ellipse2.svg'),url('../assets/images/Ellipse3.svg'),  */
    url('../assets/images/Ellipse4.svg'), url('../assets/images/Ellipse5.svg');
    background-repeat: no-repeat;
    background-position-y:
    /* 20vh, */
     /* 48vh,45vh, */
      80vh, 58vh;
    background-position-x: 
    /* 10vh, */
    /* center,center,  */
    right, right;
    background-attachment: 
    /* scroll, */
     /* scroll, scroll, */
      fixed, fixed;
}

.spending-section{
    background-image: url('../assets/images/spendingColorGroup.svg');
    background-repeat: no-repeat;
    background-position:right, 200px 0vh, center 20vh;
    background-size: contain;
    background-attachment: fixed;
}


@media screen and (max-width:485px) {
    .spending-section{
        background-attachment: scroll;
    }
}


</style>