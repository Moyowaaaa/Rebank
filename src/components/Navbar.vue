<script setup lang="ts">
import {gsap} from 'gsap'
import { onMounted,ref } from 'vue';

let show = ref<boolean>(false)

const links = ['Card','App','Pricing', 'FAQs']

var navTl = gsap.timeline()

var menuTl = gsap.timeline()

var menuBodyTl = gsap.timeline({paused:true})

onMounted(() => {
    menuTl.to('.bar1', {
        duration:0.5,
        attr:{d: "M8,2 L2,8"},
	x:1,
	ease: "power3.inOut"
    }, 'start')

    menuTl.to('.bar2',{
	autoAlpha: 0,
    duration:0.5
}, 'start')

    menuTl.to('.bar3',{
	attr:{d: "M8,8 L2,2"},
    duration:0.5,
	x:1,
	ease: "power3.inOut"
}, 'start')




menuTl.reverse()

menuBodyTl.to('.menu', {
    duration:0.5,
	display: "block",
	ease: 'Expo.easeInOut',

 
})


menuBodyTl.from('.link1', {
    opacity:0,
    duration:1.2,
    stagger: 0.2,
    y:200,
    ease:"power3.inOut"
}, "<0.1")

menuBodyTl.from('.link2', {
    opacity:0,
    duration:1.2,
    stagger: 0.4,
    y:200,
    ease:"power3.inOut"
}, "<0.1")


menuBodyTl.from('.link3', {
    opacity:0,
    duration:1.2,
    stagger: 0.6,
    y:200,
    ease:"power3.inOut"
}, "<0.1")


menuBodyTl.from('.link4', {
    opacity:0,
    duration:1.2,
    stagger: 0.8,
    y:200,
    ease:"power3.inOut"
}, "<0.1")

menuBodyTl.from('.button', {
    opacity:0,
    duration:1.2,
    stagger: 1,
    y:200,
    ease:"power3.inOut"
}, "<0.1")




menuBodyTl.reverse()


navTl.from('.navbar', {
    // opacity:0,
    // ease:"Expo.easeInOut",
    // duration:0.3,
    // delay:1.3,
    ease:"power3.inOut",
    y:-200,
    opacity:0,
    delay:1.6
})


})


const openMenu = () => {
 
    menuTl.reversed(!menuTl.reversed())
    menuBodyTl.reversed(!menuBodyTl.reversed())
    
}





</script>


<template>
    <div >
    <div class="navbar w-screen lg:w-full py-4  fixed bg-black text-white flex justify-between px-4 lg:px-10 items-center z-50">

        <div class="logo text-xl font-[grotesk-bold] cursor-pointer">REBANK</div>

        <div class="flex gap-4 hidden lg:flex cursor-pointer">
            <div class="navlinks hidden lg:flex gap-4 font-[grotesk] items-center" v-for="link in links">
            <p>{{ link }}</p>
        </div>

            <button class="navButton px-10 py-2 bg-white text-black rounded-md">Login</button>
        </div>
       

        <div class="lg:hidden nav-button z-50" @click="openMenu">
            <svg viewBox="0 0 12 10" class="hamburger" height="40px" width="40px">
                    <path d="M10,2 L2,2" class="bar1"></path>
                    <path d="M2,5 L10,5" class="bar2"></path>
                    <path d="M10,8 L2,8" class="bar3"></path>

                </svg>
        </div>

   
    </div>
    <div class="menu hidden h-screen pt-[6rem] fixed w-screen  bg-black text-white lg:hidden z-40" >

        <div class="link flex flex-col gap-6 px-4 font-[grotesk-medium]">
            <p class="link1">Card</p>

<p class="link2">App</p>

<p class="link3">Pricing</p>

<p class="link4">FAQs</p>

<button class="button px-10 py-2 bg-white text-black rounded-md ">Login</button>
        </div>
    </div>
    </div>
</template>



<style scoped>
.hamburger path{
    fill: none;
    stroke: white;
    stroke-linecap: round;
}
</style>