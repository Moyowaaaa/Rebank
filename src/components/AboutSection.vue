<template>
    <div class=" w-full h-auto flex flex-col gap-4 mb-24">

        <div class="about-section h-screen">
            <h1 class="pl-10 font-[grotesk-bold] text-lg py-6">
        Used by the world's most amazing companies
    </h1>
        <MarqueeVue />

        <div class="absolute  w-[10rem] object-cover right-0 mt-6" >
            <img src="../assets/images/showcaseColorGroup.svg" class="w-full"/>
        </div>

        <div class=" flex gap-4 absolute h-full w-full items-center " >
            <!-- <AboutImages /> -->
            <div class="w-6/12 border-2 border-[blue]"></div>


            <div class=" w-6/12 h-auto pb-8 w-[50rem]" >
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



        <div class="spending-section h-screen w-full flex" >
            <div class=" w-6/12 flex flex-col justify-center">
                <div class="w-full  px-4">
                    <p class="font-[grotesk] font-semibold">Companion App</p>
                    <h1 class="font-[grotesk-bold] text-5xl pt-3">Spending insights at your <br />
                        <div class="flex gap-2 pt-2 items-start">
                            fingertips
                            <div class="w-8/12 pt-2 flex flex-col gap-4">
                                <p class="text-base font-[grotesk]">Engineered for clarity and speed to take your everyday <br /> spending experience to the next level. Instant transfers, <br/> virtual cards and heads up displays helps give you piece of <br/> mind about your finances.</p>
                                <button class="flex border-2 rounded border-black w-max text-base font-[grotesk] py-4 px-8">
                                    Find out more
                                </button>
                            </div>
                        </div> 
             
                    </h1>
                </div>
            </div>
            <div class="absolute right-2 phones-container w-6/12 h-full ">
                
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

.spending-section{
    background-image: url('../assets/images/spendingColorGroup.svg');
    background-repeat: no-repeat;
    background-position:right, 200px 0vh, center 20vh;
    background-size: contain;
}

.phones-container{
    background-image:   url('../assets/images/spendingPink.svg'),url('../assets/images/spendingYellow.svg'),url('../assets/images/scribble2.svg');
    background-repeat: no-repeat;
    background-position-x:25rem,12rem ,0rem;
    background-position-y:15vh, 10vh, 50vh;
    background-size: auto, auto, auto;
    /* background-position-x:1rem ,center;
    background-position-y: 15vh, 10vh; */
    
    
}
</style>