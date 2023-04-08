<template>
    <div class="w-full h-auto max-h-screen    py-10 flex flex-col items-center justify-evenly gap-2 lg:gap-4" data-scroll data-scroll-section>
        <div class="pt-12">
            <img src="../assets/images/faqsTopColorGroup.svg" />
        </div>


        <div class="w-11/12 lg:w-6/12 mx-auto flex flex-col gap-2 ">

            <div class="flex flex-col gap-2 lg:gap-0 mb-10">
                <h1 class="font-[grotesk-bold] text-5xl lg:text-6xl text-center">FAQs</h1>

<p class="font-[grotesk] text-center text-sm lg:text-base">Don’t see your question here? <span class="font-[grotesk-bold]">Get in touch</span></p>

            </div>

            

            

         
            

            <div class="w-full border-b-2 border-black flex justify-between py-4 items-center text-lg font-[grotesk-medium] text-sm lg:text-base" v-for="question in questions">
                <p>{{ question }}?</p>

                <img src="../assets/images/chevronDown.svg" />
            </div>
        </div>

        <div>
            <img src="../assets/images/faqsBottomColorGroup.svg" />
        </div>

    </div>
</template>

<script setup lang="ts">
const questions:string[] = ['Are there any sign up fees','Are there any ongoing fees','Can I pay for Relume Library with this','How do I setup Apple Pay or Google Pay','How long does it take for my card to come']
</script>

<style scoped>

</style>