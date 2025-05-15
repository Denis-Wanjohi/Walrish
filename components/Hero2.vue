<template>
    <nav class="w-screen flex h-[70px] justify-between lg:gap-40  px-20 fixed z-20 bg-slate-100 opacity-90 text-[#431407] py-2 overflow-hidden">
        <a href="#">
            <img src="/image.png" class="h-full animate__animated animate__bounce" alt="">
        </a>
            <div class="sm:flex text-xl gap-5 items-center px-3 text-nowrap hidden  ">
                <a href="#about_us" class="hover:bg-amber-600 hover:px-2  hover:py-1  hover:font-bold hover:text-white  rounded">About us</a>
                <a href="#services" class="hover:bg-amber-600 hover:px-2  hover:py-1  hover:font-bold hover:text-white  rounded">Our Services</a>
                <a href="#contacts" class="hover:bg-amber-600 hover:px-2  hover:py-1  hover:font-bold hover:text-white  rounded">Contacts</a>
           </div>
        
    </nav>
    <div class="w-screen h-[90vh] " style="background-image: url('https://img.freepik.com/free-photo/building-new-concrete-house_1398-2995.jpg?uid=R159964388&ga=GA1.1.825660883.1729923843&semt=ais_hybrid&w=740');">
        <div class="w-full h-full bg-gradient-to-r from-black  ">
            <div class="flex flex-col items-center justify-center h-full  lg:w-1/2 text-center">
                <h1 class="sm:text-5xl text-3xl font-bold text-white animate__animated animate__fadeInLeft">Building Trust, Delivering Excellence.</h1>
                <p class="sm:text-md  text-white text-center sm:px-10 mt-10 lora-500 animate__animated animate__fadeInUp">At Walrish Contractors Limited, we are committed to shaping the future through reliable construction services that stand the test of time. With a focus on quality, safety, and integrity, we deliver projects that exceed expectations and strengthen communities.</p>
            </div>

        </div>
    </div>
</template>


<script setup>
import 'animate.css';
</script>