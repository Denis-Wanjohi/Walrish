<template>
 <nav class="w-full flex h-[70px] justify-between lg:gap-40  ms:px-20 px-4   bg-slate-100  text-[rgb(67,20,7)] py-2 overflow-hidden">
        <a href="/">
            <img src="/image.png" class="h-full animate__animated animate__bounce" alt="">
        </a>
            <div class="sm:flex text-xl gap-5 items-center px-3 text-nowrap hidden  ">
                <a href="#about_us" class="hover:bg-amber-600 hover:px-2  hover:py-1  hover:font-bold hover:text-white  rounded">About us</a>
                <a href="#services" class="hover:bg-amber-600 hover:px-2  hover:py-1  hover:font-bold hover:text-white  rounded">Our Services</a>
                <a href="#contacts" class="hover:bg-amber-600 hover:px-2  hover:py-1  hover:font-bold hover:text-white  rounded">Contacts</a>
           </div>
           <div class="sm:hidden flex items-center">
            <svg v-if="!menu" @click="menu = true" xmlns="http://www.w3.org/2000/svg"
                class="w-10 text-black cursor-pointer" viewBox="0 0 24 24">
                <g fill="none" stroke="currentColor" stroke-dasharray="16" stroke-dashoffset="16" stroke-linecap="round"
                    stroke-linejoin="round" stroke-width="2">
                    <path d="M5 5h14">
                        <animate fill="freeze" attributeName="stroke-dashoffset" dur="0.26s" values="16;0" />
                    </path>
                    <path d="M5 12h14">
                        <animate fill="freeze" attributeName="stroke-dashoffset" begin="0.26s" dur="0.26s"
                            values="16;0" />
                    </path>
                    <path d="M5 19h14">
                        <animate fill="freeze" attributeName="stroke-dashoffset" begin="0.52s" dur="0.26s"
                            values="16;0" />
                    </path>
                </g>
            </svg>
            <svg v-else @click="menu = false" xmlns="http://www.w3.org/2000/svg" class="w-10 text-black cursor-pointer" viewBox="0 0 24 24">
                <g fill="none" stroke="currentColor" stroke-dasharray="16" stroke-dashoffset="16" stroke-linecap="round"
                    stroke-linejoin="round" stroke-width="2">
                    <path d="M7 7l10 10">
                        <animate fill="freeze" attributeName="stroke-dashoffset" dur="0.52s" values="16;0" />
                    </path>
                    <path d="M17 7l-10 10">
                        <animate fill="freeze" attributeName="stroke-dashoffset" begin="0.52s" dur="0.52s"
                            values="16;0" />
                    </path>
                </g>
            </svg>
        </div>
        
    </nav>
    <!-- MENU -->
    <div v-if=menu class="fixed sm:hidden  top-[75px] z-30 w-fit px-7 right-0 mr-3 bg-white text-black pt-5 rounded-xl  text-2xl font-serif">
        <div @click="nextPage('services')" class="flex gap-4 items-center font-bold py-2 border-b">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                <path fill="currentColor"
                    d="m9.108 11.758l2.284-2.29l-2.053-2.06L8.18 8.566l-.708-.708L8.625 6.7L6.673 4.748l-2.29 2.29zm7.834 7.84l2.29-2.29l-1.951-1.952l-1.158 1.152l-.707-.708l1.151-1.158l-2.04-2.034l-2.285 2.284zM17.273 5l1.733 1.733zM7.153 20H4v-3.154l4.394-4.394L3 7.039l3.673-3.673l5.439 5.419l5.205-5.212l3.085 3.173l-5.142 5.168l5.375 5.413L16.96 21l-5.413-5.394zM5 19h1.727l9.82-9.814l-1.734-1.732L5 17.273zM15.692 8.314l-.878-.86l1.732 1.733z" />
            </svg>
            <p>Our Services</p>
        </div>
        <div @click="nextPage('about_us')"  class="flex gap-4 items-center font-bold py-2 border-b">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                <path fill="currentColor"
                    d="M11 9h2V7h-2m1 13c-4.41 0-8-3.59-8-8s3.59-8 8-8s8 3.59 8 8s-3.59 8-8 8m0-18A10 10 0 0 0 2 12a10 10 0 0 0 10 10a10 10 0 0 0 10-10A10 10 0 0 0 12 2m-1 15h2v-6h-2z" />
            </svg>
            <p>About us</p>
        </div>
        <div @click="useRouter().push('/projects/Modern_Office_Space_Renovation_-_CBD_Towers')"  class="flex gap-4 items-center font-bold  py-2 border-b">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                <g fill="none" stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                    color="currentColor">
                    <path
                        d="m13 11l5-5m1 1l-2-2l2.5-1.5l1 1zM4.025 8.975a3.5 3.5 0 0 1-.79-3.74l1.422 1.422h2v-2L5.235 3.235a3.5 3.5 0 0 1 4.529 4.53l6.47 6.471a3.5 3.5 0 0 1 4.53 4.529l-1.421-1.422h-2v2l1.422 1.422a3.5 3.5 0 0 1-4.53-4.528L7.763 9.765a3.5 3.5 0 0 1-3.738-.79" />
                    <path
                        d="m12.203 14.5l-5.604 5.604a1.35 1.35 0 0 1-1.911 0l-.792-.792a1.35 1.35 0 0 1 0-1.911L9.5 11.797" />
                </g>
            </svg>
            <p>Projects</p>
        </div>
        <div @click="nextPage('contacts')"  class="flex gap-4 items-center font-bold py-2">
            <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                <path fill="currentColor"
                    d="M6.62 10.79c1.44 2.83 3.76 5.14 6.59 6.59l2.2-2.2c.27-.27.67-.36 1.02-.24c1.12.37 2.33.57 3.57.57c.55 0 1 .45 1 1V20c0 .55-.45 1-1 1c-9.39 0-17-7.61-17-17c0-.55.45-1 1-1h3.5c.55 0 1 .45 1 1c0 1.25.2 2.45.57 3.57c.11.35.03.74-.25 1.02z" />
            </svg>
            <p>Contact us</p>
        </div>
    </div>
</template>

<script setup>
const menu = ref(false)
function nextPage(section){
    useRouter().push('/?section='+section)
}
</script>