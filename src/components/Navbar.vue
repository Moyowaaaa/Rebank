<template>
    <div class="w-screen lg:w-full py-4  fixed bg-black text-white flex justify-between px-4 lg:px-10 items-center z-30">

        <div class="text-xl font-[grotesk-bold]">REBANK</div>
        
        <div class="hidden lg:flex gap-4 font-[grotesk] items-center">
            <p>Card</p>

            <p>App</p>

            <p>Pricing</p>

            <p>FAQs</p>

            <button class="px-10 py-2 bg-white text-black rounded-md">Login</button>
        </div>

        <div class="lg:hidden">
            <svg viewBox="0 0 12 10" class="hamburger" height="40px" width="40px">
                    <path d="M10,2 L2,2" class="bar1"></path>
                    <path d="M2,5 L10,5" class="bar2"></path>
                    <path d="M10,8 L2,8" class="bar3"></path>

                </svg>
        </div>
    </div>
</template>

<script setup lang="ts">

</script>

<style scoped>
.hamburger path{
    fill: none;
    stroke: white;
    stroke-linecap: round;
}
</style>