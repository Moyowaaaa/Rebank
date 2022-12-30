<template>
    <div class="about w-full h-auto  flex flex-col gap-4 ">

        <div class="about-section  min-h-screen">
            <h1 class="pl-10 font-[grotesk-bold] text-lg py-6">
        Used by the world's most amazing companies
    </h1>
        <MarqueeVue />

        <div class="absolute  w-[10rem] object-cover right-0 mt-6" >
            <img src="../assets/images/showcaseColorGroup.svg" class="w-full"/>
        </div>


        <div class="w-full mt-[8rem] flex  gap-6 ">
            <div class="w-7/12 ">
                <div class="flex my-32">
            <img src="../assets/images/showcaseOrange.svg" />
            <img src="../assets/images/showCaseYellow.svg" />
        </div>


        <div class="relative bottom-[56rem] flex flex-col  h-[5rem] w-max justify-between left-[28rem] gap-32">
            <img src="../assets/images/showcaseBlue.svg" />
            <img src="../assets/images/showcasePink.svg" />
        </div>

        <div class="-z-50 relative bottom-[29.5rem] flex flex-col  h-[5rem] w-max justify-between left-[25rem] ">
            <img src="../assets/images/Ellipse1.svg" class="w-[5.2rem] relative left-[13rem] bottom-[15rem]"/>

            <div class="flex flex-col items-center">
                <img src="../assets/images/Ellipse2.svg" class="relative top-[8.5rem] w-[7rem]" />
                <img src="../assets/images/Ellipse3.svg" class="w-[10rem]"/>
            </div>
            
        </div>
            </div>


            <div class="w-7/12 flex flex-col justify-end pb-64">
                <div class="flex flex-col gap-4">
            <p class="font-[grotesk-medium]">Physical Card</p>
            <h1 class="text-6xl font-[grotesk-bold] w-[45rem]">Spend anywhere with a physical debit card</h1>
            <p class="text-lg font-[grotesk] w-[39rem] text-justify">The debit card is designed to spend everywhere and everywhere with simplicity and transparency built in. An RFID transponder embedded in its core enables you to pay with a quick touch-free wave.</p>
      

            <button class=" w-max py-4 px-6 rounded border-2 border-black font-[grotesk]">Find out more</button>
        </div>
            </div>
        </div>


        </div>


        <div class="spending-section min-h-screen  w-full flex flex-col my-6 items-center mb-42">

            <div class="flex gap-4  items-center w-full ">
                <div class="w-6/12  flex flex-col items-start pl-4" >
                    <p class="font-[grotesk-medium]">Companion App</p>
                    <h1 class="text-6xl font-[grotesk-bold] w-[50rem]">Spending insights at your</h1>
                    <div class="flex gap-6 items-start">
                        <h1 class="text-6xl font-[grotesk-bold]">fingertips</h1>
                        <p class="text-base font-[grotesk] pt-4">Engineered for clarity and speed to take your everyday spending experience to the next level. Instant transfers, virtual cards and heads up displays helps give you piece of mind about your finances.</p>
                    </div>
                </div>


                <div class="w-6/12  flex items-center justify-center h-[50rem]">
                    <img src="../assets/images/scribble2.svg" class="relative  self-end left-[6.5rem] bottom-6"/>
                    <img src="../assets/images/spendingYellow.svg" class="relative my-32 right-32"/>
                    <img src="../assets/images/spendingPink.svg" class="relative right-48 top-12"/>
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



</style>