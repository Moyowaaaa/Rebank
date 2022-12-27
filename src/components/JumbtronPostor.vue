<template>
    <div class="jumbotron h-screen bg-black text-white  flex flex-col items-center justify-center">

        <div class="w-7/12 flex flex-col py-4 gap-4">
            <div class="w-full flex justify-start">
                <p class="font-[roboto-medium]">Personalisation</p>
            </div>
            <h1 class="flex text-center text-5xl font-[grotesk-bold] z-20">Stand out from the crowd with a card <br/> and app to match your style</h1>
            <div class="relative left-[40rem] bottom-10 w-max">
                <img src="../assets/images/scribble.svg" />
            </div>
            <p class="text-center font-[roboto]">
                Don’t blend into the crowd with a boring bank card, stand out! Choose a card colour to suit your style <br/> and the app will change to match.
            </p>

            <div class="w-full flex justify-center">
                <button class="flex border-2 border-white rounded py-4 px-8 font-[roboto]">
                    Find out more
                </button>
            </div>
        </div>
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.jumbotron{
    background-image: url('../assets/images/jumbotronLeft.svg'), url('../assets/images/jumbotronRight.svg');
    background-repeat:  no-repeat;
    background-size: contain contain;
    background-position: bottom left, bottom right;
    background-attachment: fixed, fixed;
}
</style>