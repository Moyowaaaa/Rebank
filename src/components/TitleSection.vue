<template>
    <div class="title-section flex w-full  h-screen pt-[5rem]">
     

        <div class=" flex flex-col w-full justify-center ">

            <div class="w-full  h-5/6 absolute my-12 flex justify-between items-end pb-24 pr-10" >
                <div class="h-auto">
                    <img src="../assets/images/titleColorGroup.svg" />
                </div>


                <div class="h-auto flex gap-2 pb-28">
                
                    <img src="../assets/images/lineShort.svg" />
                    <img src="../assets/images/lineMedium.svg" />
                    <img src="../assets/images/lineTall.svg" />
                </div>
            </div>


            <div class="h-full w-full  pl-24 flex flex-col justify-center" >
                <div class="flex flex-col gap-4">
                    <h1 class="text-6xl font-bold font-[grotesk-bold]">Welcome to <br/> personalised banking</h1>

                    <div class="w-max text-xl">
                        More than a debit card, we’ve redesigned and reimagined the entire <br/> idea of banking. Spend securely. Pay anyway you want. Get insights <br/> about your money. Welcome to banking revolving around you.
                    </div>


                    <div class=" py-6 flex gap-4">

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

<script setup lang="ts">

</script>

<style scoped>
.title-section {
    background-image:url('../assets/images/titleSectionMain.svg'), url('../assets/images/starBig.svg'), url('../assets/images/starYellow.svg'), url('../assets/images/starPurple.svg'), url('../assets/images/starBlue.svg');
    background-repeat: no-repeat;
    
    background-position:right,100px 200px, 20vh 62vh, 70rem 44rem, 500px 300px;
    background-size: contain, auto, auto, auto,auto;

}
</style>