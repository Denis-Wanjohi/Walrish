<template>
    <header>
       <div class="w-fit mx-auto rounded-2xl flex gap-10 bg-red-300 h-[50px] overflow-hidden">
           <img src="/image.png" class="" alt="walrish"> 
           <div class="flex text-xl gap-5 items-center px-3 ">
                <p>About us</p>
                <p>Our Services</p>
                <p>Contacts</p>
           </div>
       </div>
    </header>
    
    <div class="text-white w-10/12 mx-auto mt-10 h-[200vh]">
        <div class="flex">
            <img class="w-2/3" src="/image.png" alt="walrish">
            <h1 class="w-1/3 cinzel-decorative-bold text-6xl text-center my-auto leading-30">WALRISH CONTACTORS</h1>
        </div>
        <div class="flex">
            <div class="w-2/3">
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Nulla dolorem expedita architecto quidem, eos mollitia. A cupiditate expedita fuga esse quia, tempore accusantium assumenda blanditiis labore repudiandae tenetur recusandae temporibus.</p>
                <h2 class="text-center lora-normal text-3xl  my-5">General Construction Services</h2>
            </div>
            <img class="w-1/3" src="/image.png" alt="walrish">
        </div>
    </div>
</template>

<script setup>
import { useScroll,useMotionValue,Motion } from 'motion-v'
const { scrollY } = useScroll()
const { scrollYProgress } = useScroll();
useMotionValue(scrollY, 'change', (latest) => {
  console.log('Page scroll: ', latest)
})
</script>