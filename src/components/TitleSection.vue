<script setup lang="ts">
import gsap from 'gsap';
import { onMounted } from 'vue';

onMounted(() => {
    const titleTl = gsap.timeline()

   
    titleTl.fromTo('.title-head',{opacity:0},{ y: 0, opacity: 1, duration:1.5, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)" },'<0.1');
    titleTl.from('.title-content', {
        duration:0.5,
        ease:"power3.inOut",
        opacity:0,

        
    })
    titleTl.fromTo('.bars',{opacity:0},{ y: 0, opacity: 1, duration:1.5, delay:0.8, clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)" });

    titleTl.to('.color-group',{
        scaleY:1.2,
        duration:0.6,
        opacity:1,
        ease:"power3.inOut"
    },"<0.1")
})


</script>


<template>
    <div class="title-section flex w-screen lg:w-full  h-screen pt-[5rem] ">
     

        <div class="title-content flex flex-col w-full justify-center ">

            <div class="w-full  h-5/6 absolute my-12 flex justify-between items-end pb-24 lg:pr-10" >
                <div class="opacity-0 color-group hidden lg:flex h-auto">
                    <img src="../assets/images/titleColorGroup.svg" />
                </div>


                <div class="bars hidden h-auto lg:flex gap-2 pb-28">
                
                    <img src="../assets/images/lineShort.svg" />
                    <img src="../assets/images/lineMedium.svg" />
                    <img src="../assets/images/lineTall.svg" />
                </div>
            </div>


            <div class="h-full w-screen lg:w-full  lg:pl-24 flex flex-col justify-center" >
                <div class="flex flex-col gap-4 ">
                    <h1 class="title-head text-5xl lg:text-6xl font-bold font-[grotesk-bold] w-11/12 mx-auto lg:w-[45rem] lg:mx-0">Welcome to personalised banking</h1>

                    <div class="w-full text-base w-11/12 mx-auto lg:text-xl lg:w-[40rem] lg:text-justify lg:mx-0">
                        More than a debit card, we’ve redesigned and reimagined the entire idea of banking. Spend securely. Pay anyway you want. Get insights  about your money. Welcome to banking revolving around you.
                    </div>


                    <div class=" py-6 flex gap-4 flex-col lg:flex-row w-11/12 lg:w-full mx-auto lg:mx-0">

                        <button class="py-4 px-8 flex items-center justify-center bg-black text-white rounded-md">
                            Get started
                        </button>

                        <button class="py-4 px-8 flex items-center justify-center text-black border-2 border-black rounded-md gap-2 ">
                            <p>Find out more</p>
                            <img src="../assets/images/down.svg" />
                        </button>
                    </div>
                </div>
            </div>
           
      
           
        </div>
    </div>
</template>



<style scoped>
.title-section {
    background-image:url('../assets/images/titleSectionMain.svg'), url('../assets/images/starBig.svg'), url('../assets/images/starYellow.svg'), url('../assets/images/starPurple.svg'), url('../assets/images/starBlue.svg');
    background-repeat: no-repeat;
    
    background-position:right,100px 200px, 20vh 62vh, 70rem 44rem, 500px 300px;
    background-size: contain, auto, auto, auto,auto;

}


@media screen and (max-width:485px) {
.title-section{
background-image: none;
}
}
</style>