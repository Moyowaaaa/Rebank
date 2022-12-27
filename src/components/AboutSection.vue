<template>
    <div class="about-section w-full min-h-screen h-auto">
        <h1 class="pl-10 font-[grotesk-bold] text-lg py-6">
        Used by the world's most amazing companies
    </h1>
        <MarqueeVue />

        <div class="absolute  w-[10rem] object-cover right-0 mt-6" >
            <img src="../assets/images/showcaseColorGroup.svg" class="w-full"/>
        </div>

        <div class=" flex gap-4 absolute h-full w-full items-center " >
            <AboutImages />


            <div class=" w-6/12 self-end h-auto pb-8 w-[50rem]" >
                <div class="flex flex-col  w-10/12 gap-4">
                    <h1 class=" font-[grotesk-bold] text-lg py-6">
        Physical Card
    </h1>
    <h2 class="text-5xl font-[grotesk-bold]">Spend anywhere with a <br /> physical
         debit card</h2>

         <p>The debit card is designed to spend everywhere and everywhere with <br/> simplicity and transparency built in. An RFID transponder embedded in <br/> its core enables you to pay with a quick touch-free wave.</p>

         <button class="flex py-4 px-8 border-2 rounded border-black w-max">
            <p class="font-[grotesk-light]">Find out more</p>
         </button>
                </div>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">
import MarqueeVue from './Marquee.vue';
import AboutImages from '../components/AboutImages.vue'
</script>

<style scoped>


.about-section {
    background-image:url('../assets/images/Ellipse1.svg'), url('../assets/images/Ellipse2.svg'),url('../assets/images/Ellipse3.svg'), url('../assets/images/Ellipse4.svg'), url('../assets/images/Ellipse5.svg');
    background-repeat: no-repeat;
    background-position-y:20vh, 48vh, 45vh, 80vh, 58vh;
    background-position-x: center,center,center, right, right;
    background-attachment: scroll, scroll, scroll, fixed, fixed;
}
</style>