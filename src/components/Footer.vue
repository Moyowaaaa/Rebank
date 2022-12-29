<template>
    <div class="w-full h-[20rem]">
        <div class="px-10 w-full py-4  h-full flex justify-between">
        <div class="text-xl font-[grotesk-bold]">REBANK</div>

        <div class="flex flex-col gap-2">


            <div class="flex gap-20 px-6">
            

                <div class="flex flex-col gap-2">
                    <div v-for="about in aboutLinks" class="flex flex-col gap-4">
                    <p class="text-xl font-[grotesk-bold]">{{ about.title }}</p>    


                    <div v-for="aboutLink in aboutLinks[0].links">
                    <p class="font-[grotesk]">{{ aboutLink }}</p>
                    </div>
                    </div>
                </div>

                <div class="flex flex-col gap-2">
                    <div v-for="card in cardLinks" class="flex flex-col gap-4">
                    <p class="text-xl font-[grotesk-bold]">{{ card.title }}</p>    


                    <div v-for="cardLink in cardLinks[0].links">
                    <p class="font-[grotesk]">{{ cardLink }}</p>
                    </div>
                    </div>
                </div>


                <div class="flex flex-col gap-2">
                    <div v-for="app in appLinks" class="flex flex-col gap-4">
                    <p class="text-xl font-[grotesk-bold]">{{ app.title }}</p>    


                    <div v-for="appLink in appLinks[0].links">
                    <p class="font-[grotesk]">{{ appLink }}</p>
                    </div>
                    </div>
                </div>


            </div>
            
           
           
        </div>
        


        <div class=" flex flex-col flex flex-col gap-2">
            <h2 class="text-xl font-[grotesk-bold]">Subscribe</h2>
            <p class="font-[grotesk]">Join our newsletter to stay up to date on features and releases.</p>

            <div class="flex w-full  gap-4">
                <input type="text" 
                class="rounded border-2 border-black py-2 px-4 w-9/12 placeholder:font-[grotesk-light]" 
                placeholder="Enter your email"
                />

                <button class="py-4 px-6 border-2 border-black rounded w-3/12 font-[grotesk] flex items-center justify-center">Subscribe</button>
            </div>
            <p class="text-sm w-[36rem] font-[grotesk-light]">By subscribing you agree to with our <span class="underline">Privacy Policy</span> and provide consent to receive updates from our company.</p>
        </div>


        
    </div>
    
    <div class="pb-12 mx-10 pb-4 pt-6 flex items-center gap-4 justify-between border-t-2 border-black">
        <div class="flex gap-4 h-full items-center font-[grotesk]">
        <p class="underline">2022 Rebank. All right reserved.</p>
        <p class="underline">Privacy Policy</p>
        <p class="underline">Terms of Service</p>
        <p class="underline">Cookies Settings</p>
        </div>


        <div class="flex gap-4 h-full items-center">
            <img src="../assets/images/Facebook.svg" />
            <img src="../assets/images/Instagram.svg" />
            <img src="../assets/images/Twitter.svg" />
            <img src="../assets/images/LinkedIn.svg" />
        </div>
     
    </div>



    <div class="absolute w-max right-0 ">
            <img src="../assets/images/footerColorGroup.svg" />
        </div>
  
    </div>
</template>

<script setup lang="ts">
import { ref } from 'vue';
const aboutLinks = [{
    title:'About',
    links:['Pricing','FAQ','Contact','News']
}]

const cardLinks = [{
    title:'Card',
    links:['About','Colours','Replacement','Freeze']
}]

const appLinks = [{
    title: 'App',
    links:['Download','Virtual Cards', 'Transfers', 'Lock Cards']
}]


</script>

<style scoped>

</style>