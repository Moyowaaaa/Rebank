<template>
    <div class="title-section flex w-screen  h-screen pt-[5rem]">
     

        <div class=" flex flex-col w-full  border-2 border-[red] justify-center ">
           
           
            <div class="flex gap-6">
                <!-- <div class="flex flex-col   absolute justify-end bottom-[5rem]">
                    <img src="../assets/images/titleColorGroup.svg" />
                </div>
                 -->

                <div class="flex flex-col gap-4 ml-[6rem] border-2 border-[red] h-full ">
                    
                    <h2 class="text-6xl font-[grotesk-bold] ">
                        Welcome to  <br /> personalised banking
                    </h2>

                    <div class="text-xl font-[grotesk] ">
                        <p>More than a debit card, we’ve redesigned and reimagined the entire <br/> idea of banking. Spend securely. Pay anyway you want. Get insights <br/> about your money. Welcome to banking revolving around you.</p>
                    </div>


                    <div class="flex  gap-4 font-[grotesk-light]">
                        <button class="py-4 px-8 bg-black text-white rounded-md">Get started</button>

                        <button class="flex gap-4 items-center py-4 px-8 border-2 border-black rounded-md"><p>Find out more</p> <img src="../assets/images/down.svg" /></button>
                    </div>


                   
                </div>
                
            </div>
           
        </div>
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.title-section {
    background-image:url('../assets/images/titleSectionMain.svg');
    background-repeat: no-repeat;
    background-position:right;   
    background-size: contain;
}
</style>