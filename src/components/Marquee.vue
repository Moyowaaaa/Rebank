<template>
    <div class="w-full z-50">
    <Vue3Marquee class="overflow-hidden h-auto">
    <div class="w-full  flex items-center gap-12 pl-4">
        <div  v-for="(image, index) in marqueArray">
        <img :src="image" :key="index"/>
        </div>

        <div class="flex gap-12 pl-4">
            <img :src="image" v-for="image in marqueArray" :key="image"  />
        </div>
       
    </div>

    </Vue3Marquee>
    </div>  
</template>

<script setup lang="ts">
import { Vue3Marquee } from 'vue3-marquee'
import 'vue3-marquee/dist/style.css'
import spline from '../assets/images/spline.svg'
import untitledUI from '../assets/images/untitledUI.svg'
import relume from '../assets/images/relume.svg'
import flowNinja from '../assets/images/flowNinja.svg'
import webflow from '../assets/images/webflow.svg'


const marqueArray = [spline,untitledUI,relume,flowNinja,webflow]

</script>

<style scoped>
.word {
  font-size: 30px;
  margin: 0 10px;
}
.odd {
  color: rgb(68, 77, 84);
}
.even {
  color: rgb(137, 147, 156);
}
</style>