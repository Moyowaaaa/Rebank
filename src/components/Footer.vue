<template>
    <div class="w-full h-auto lg:h-[20rem]">
        <div class="lg:px-10 w-full py-4  h-full flex flex-col lg:flex-row lg:justify-between">
        <div class="text-xl font-[grotesk-bold] pl-4 lg:pl-0 pb-10 lg:pb-0">REBANK</div>

        <div class="flex flex-col gap-2">


            <div class="flex flex-row flex-wrap gap-20 px-4 lg:px-6">
            

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
        


        <div class=" flex flex-col flex flex-col gap-2 pt-8 lg:pt-0">
            <h2 class="text-base lg:text-xl font-[grotesk-bold] pl-4">Subscribe</h2>
            <p class="text-sm lg:text-base font-[grotesk] pl-4">Join our newsletter to stay up to date on features and releases.</p>

            <div class="flex flex-col lg:flex-row w-full w-11/12 mx-auto lg:mx-0  gap-4">
                <input type="text" 
                class="rounded border-2 border-black py-2 px-4 w-full lg:w-9/12 placeholder:font-[grotesk-light]" 
                placeholder="Enter your email"
                />

                <button class="py-2 lg:py-4 px-6 border-2 border-black rounded w-full lg:w-3/12 font-[grotesk] flex items-center justify-center">Subscribe</button>
            </div>
            <p class="text-xs lg:text-sm w-11/12 mx-auto lg:mx-0 lg:w-[36rem] font-[grotesk-light]">By subscribing you agree to with our <span class="underline">Privacy Policy</span> and provide consent to receive updates from our company.</p>
        </div>


        
    </div>
    
    <div class="pb-12 lg:mx-10 pb-4 pt-6 flex flex-col lg:flex-row lg:items-center gap-4 lg:justify-between border-t-2 border-black mx-4">
        <div class="text-sm lg:text-base flex gap-4 h-full lg:items-center font-[grotesk] flex-col lg:flex-row ">
        <p class="underline flex items-center "><span>{{ year }}</span>&nbsp;Rebank. All right reserved.</p>
        <p class="underline">Privacy Policy</p>
        <p class="underline">Terms of Service</p>
        <p class="underline">Cookies Settings</p>
        </div>


        <div class="flex gap-4 h-full items-center justify-center lg:justify-start">
            <img src="../assets/images/Facebook.svg" />
            <img src="../assets/images/Instagram.svg" />
            <img src="../assets/images/Twitter.svg" />
            <img src="../assets/images/LinkedIn.svg" />
        </div>
     
    </div>



    <div class="flex absolute w-max right-0 ">
            <img src="../assets/images/footerColorGroup.svg" />
        </div>
  
    </div>
</template>

<script setup lang="ts">
import { ref,onMounted } from 'vue';
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

let year = ref<any>()
onMounted(()=> {
    const date = new Date();
   year.value = date.getFullYear()
})


</script>

<style scoped>

</style>