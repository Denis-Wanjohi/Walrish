<template>
   
    <div class="text-center text-white font-bold sm:text-5xl text-3xl shadow-sm py-3 mx-auto">
        Projects
    </div>
    <div class="overflow-x-auto hide-scrollbar">
        <div class="flex space-x-4">
            <div class="min-w-[400px] object-cover  h-fit flex justify-center shadow-md rounded-lg p-6"
                data-aos="zoom-in" v-for="(project, key) in projects" :key="key" @mouseover="mouseOn(key)"
                @mouseleave="mouseOut()" @click="useRouter().push('/projects/'+project.title.replaceAll(' ','_'))">
                <div style=""
                    class=" cursor-pointer lora-400 rounded-xl border  overflow-y-auto hide-scrollbar pt-5 px-3 text-md ">
                    <img class="h-full mx-auto object-cover"
                        :src=project.image
                        alt="warlish">
                    <p v-if="show && key == index" class="font-bold  text-black text-2xl 
              h-full w-full  absolute top-0 text-center flex items-center
            ">
            <span class="w-3/4 font-bold">{{ project.title }}</span>
            </p>
                </div>
            </div>
        </div>
    </div>
    <div class="flex justify-center text-blue-400 gap-10">
        <p v-for="(dot, key) in 4" :key="key" :class="[index == key ? 'text-xl' : '']"> - </p>
    </div>
</template>
<script setup>
const show = ref(false)
const index = ref(null)
function mouseOn(i) {
    index.value = i
    show.value = true;
}
function mouseOut() {
    index.value = null
    show.value = false;
}
const projects = [
    
        {
            "title": "Modern Office Space Renovation - CBD Towers",
            "desc": "Walrish Contractors LTD undertook a comprehensive interior renovation of a 500 sq. meter office floor in CBD Towers. This included a complete overhaul of the interior layout to create open-plan workspaces, new meeting rooms, and a modern kitchenette. Our team handled all aspects of the renovation, including new electrical wiring for enhanced data and power access, installation of energy-efficient LED lighting, and upgrading the plumbing systems for the new kitchen and restrooms. The project was completed on schedule, delivering a vibrant and highly functional modern workspace.",
            "image":'https://media.gettyimages.com/id/2219657920/photo/modern-office-interior-with-white-desks-and-clean-design.jpg?s=612x612&w=0&k=20&c=FMLrbr1p_OU6Lc4S2beptMQjEpiKXQapjcv9OlniFOU='

        },
        {
            "title": "Residential Villa Construction - Runda Estate",
            "desc": "We successfully completed the construction of a luxurious 5-bedroom residential villa in the prestigious Runda Estate. From groundbreaking to final finishes, Walrish Contractors LTD managed the entire construction process. This included laying robust foundations, erecting the structural framework, installing the roof, and executing high-quality finishing works such as bespoke cabinetry, tiling, and painting. Our meticulous project management ensured adherence to design specifications, budget, and timelines, resulting in a beautiful and durable family home.",
            "image":'https://img.freepik.com/premium-photo/house-construction-with-autoclaved-aerated-concrete-block-structure-building-site_293060-3280.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740',
        },
        {
            "title": "School Building Rehabilitation & Accessibility Upgrade - Greenhill Academy",
            "desc": "Walrish Contractors LTD was contracted to rehabilitate an aging classroom block at Greenhill Academy. The project involved extensive structural repairs, roof replacement, and general building maintenance to ensure a safe learning environment. A key component of this project was the implementation of accessibility upgrades, including the installation of ramps and accessible restroom facilities, to ensure the building was inclusive for all students. The rehabilitation significantly extended the lifespan of the building and improved its functionality.",
            "image":'https://img.freepik.com/premium-photo/hotel-walkway-with-light-flare_91566-753.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740',
        },
        {
            "title": "Industrial Warehouse Electrical & Plumbing Upgrade - Athi River EPZ",
            "desc": "For a major logistics company in the Athi River EPZ, Walrish Contractors LTD executed a critical electrical and plumbing upgrade for their 2,000 sq. meter warehouse. This involved upgrading the entire electrical distribution system to accommodate new machinery, installing heavy-duty lighting, and overhauling the fire suppression plumbing lines. We also installed new water and drainage systems for the staff facilities. Our expertise ensured minimal disruption to the client's operations while delivering a robust and compliant infrastructure.",
            "image":'https://img.freepik.com/premium-photo/male-worker-painted-gray-pipeline-oil-flowing-valve_478515-2789.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740'
        }
    
]
</script>