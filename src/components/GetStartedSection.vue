<template>
  <div
    class="overflow-y-hidden get-started min-h-screen flex flex-col lg:flex-row w-full lg:justify-center"
  >
    <!-- <div class="absolute  h-full w-6/12 border-2 border-[teal]"></div>
        

        <div class="relative h-full border-2 border-[red] flex w-4/12 items-center right-20">
            <img src="../assets/images/getStartedPhone.svg" class="absolute w-auto z-20"/>
            <img src="../assets/images/getStartedCard.svg" class="absolute w-auto left-52"/>
        </div> -->

    <div
      class="w-full lg:w-10/12 flex flex-col lg:flex-row lg:justify-center mt-12 lg:mt-0"
    >
      <div
        class="hero flex w-11/12 lg:w-6/12 flex flex-col lg:justify-center items-center lg:items-start"
      >
        <div class="flex flex-col">
          <h2
            class="text-3xl lg:text-5xl font-[grotesk-bold] z-20 lg:w-[40rem] w-11/12 mx-auto"
          >
            Take your savings to the next level today
          </h2>
          <div class="relative hidden lg:flex lg:bottom-20 lg:right-24 w-8/12">
            <img src="../assets/images/scribble3.svg" />
          </div>
        </div>

        <p class="pb-6 text-sm lg:text-lg w-11/12 mx-auto lg:w-full">
          Get started today and take your financial control into the future.
        </p>

        <button class="py-4 px-6 bg-black text-white w-max rounded">
          Get started
        </button>
      </div>

      <div class="phone w-full lg:w-3/12 flex items-center mt-[6rem] lg:mt-0">
        <img
          src="../assets/images/getStartedCard.svg"
          class="relative left-6 lg:left-52"
        />

        <img src="../assets/images/getStartedPhone.svg" class="absolute" />
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
import { gsap } from "gsap";
import ScrollTrigger from "gsap/ScrollTrigger";
import { onMounted } from "vue";
gsap.registerPlugin(ScrollTrigger);

onMounted(() => {
  let getStartedTl = gsap.timeline({
    scrollTrigger: {
      trigger: ".get-started",
      start: "top center",
      end: "top +=10",

      scrub: 0.1,
    },
  });

  getStartedTl.from(".phone", {
    opacity: 0,
    y: 300,
    duration: 1.2,
    ease: "power3.inOut",
  });
  getStartedTl.fromTo(
    ".hero",
    { opacity: 0,scaleX:0.8 },
    {
      y: 0,
      opacity: 1,
      duration: 1.5,
    //   clipPath: "polygon(0 100%, 100% 100%, 100% 0, 0 0)",
    scaleX: 1, 
    z: -500
    },
    "<0.1"
  );
});
</script>

<style scoped></style>
