<template>
    <div class="w-full bg-black text-white h-fit">
        <h2 class=" lg:text-[100px] md:text-[70px] text-[50px] jost-900 text-white  absolute md:left-[40%] left-[10%] animate__animated animate__fadeInDown">ABOUT US</h2>
        <div class="w-full h-full md:flex">
            <div class="md:w-1/2 md:block hidden ">
                <img
                class="w-full h-full object-cover" 
                :src="image"
                alt="walrish_contractors">
            </div>
            <div class="lg:pl-10  px-5 pt-30 md:w-1/2" >
                <h2 class="cinzel-700 text-center text-2xl  text-[#FFA500]  animate__animated animate__zoomIn">Crafting Structures, Creating Futures</h2>
                <p class="lora-500 text-sm leading-6">We are committed to shaping environments that stand the test of time. Our mission is to turn your ideas into strong, functional structures through expert planning, quality craftsmanship, and dependable project execution.

                    We take pride in building not just structures, but lasting relationships with our clients and
                    communities.</p>
                <h3 class="cinzel-500 mt-10">Our Key Strengths</h3>
                <div v-for="(strength,index) in keyStrengths" :key="index">
                    <p class="text-sm"> - {{ strength }}</p>
                </div>

            </div>
            <div class="md:w-1/2 md:hidden block ">
                <img
                class="w-full h-full object-cover" 
                :src="image"
                alt="walrish_contractors">
            </div>
        
        </div>
    </div>
</template>

<script setup>
const keyStrengths = [
  "We offer personalized consultations to understand your project goals.",
  "Our team consists of skilled engineers, builders, and project managers.",
  "We partner with reputable suppliers and subcontractors to ensure excellence in every detail."
];
const image = ref('https://img.freepik.com/free-photo/different-electrical-tools-wooden-background-flat-lay_169016-25060.jpg?uid=R159964388&ga=GA1.1.825660883.1729923843&semt=ais_hybrid&w=740')
const images = [
    'https://media.gettyimages.com/id/149294470/photo/architecture-blueprint-detail.jpg?s=612x612&w=0&k=20&c=y1mk2qWShR-fEJtbhy7R_1BEvoFh3ul3XikJIaR29Ys=',
    'https://media.gettyimages.com/id/171591945/photo/plumbers-tools.jpg?s=612x612&w=0&k=20&c=1R_HDXrIsAYxPeBNVYwM-S4kWz7xhZnun2rmMAbdUf0=',
    'https://img.freepik.com/free-photo/safety-tools-painting-work_23-2148908402.jpg?uid=R159964388&ga=GA1.1.825660883.1729923843&semt=ais_hybrid&w=740',
    'https://img.freepik.com/free-photo/different-electrical-tools-wooden-background-flat-lay_169016-25060.jpg?uid=R159964388&ga=GA1.1.825660883.1729923843&semt=ais_hybrid&w=740'
]
onMounted(() => {
    setInterval(() => {
        image.value = images[Math.floor(Math.random() * images.length)]
    }, 5000)
})
</script>