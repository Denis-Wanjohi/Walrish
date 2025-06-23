<template>
    <div class="bg-black text-white md:pb-20 min:h-screen">
        <Nav-Bar></Nav-Bar>
        <div>
            <div class="w-screen h-[200px] text-center flex items-center justify-center">
                <p class="lg:text-6xl md:text-4xl text-3xl jost-900">{{ projects[id].title }} </p>
            </div>
            <div class="md:flex flex-row-reverse  w-screen sm:px-10 px-3">
                <div class="md:w-1/2 flex flex-direction gap-2 items-center">
                    <div class="px-2 overflow-hidden flex flex-col ">
                        <img :class="[image == key ? 'bg-blue-900' : '']" class="w-[150px] p-1"
                            v-for="(x, key) in projects[id].images" :key="key" :src=x alt="walrish"
                            @click="image = key">
                    </div>
                    <div>
                        <img :src=projects[id].images[image] alt="walrish">
                    </div>
                </div>
                <div class="md:w-1/2 flex items-center text-center justify-between  lg:px-10 flex-col">
                    <p>{{ projects[id].desc }}</p>
                    <div class="flex sm:w-3/4 w-screen justify-around my-5">
                        <div v-if="id !== 0" @click="id--"
                            class="px-2 py-2 bg-blue-400 w-[100px] text-center hover:bg-blue-600 rounded font-bold text-white cursor-pointer">
                            Previous</div>
                        <div v-if="id !== 3" @click="id++"
                            class="px-2 py-2 bg-blue-400 rounded font-bold w-[100px] text-center hover:bg-blue-600 text-white cursor-pointer">
                            Next</div>
                    </div>
                </div>

            </div>
        </div>
    </div>
    <Footer id="contacts" />

</template>
<script setup>
const projects = ref([
    {
        "title": "Modern Office Space Renovation - CBD Towers",
        "desc": "Walrish Contractors LTD undertook a comprehensive interior renovation of a 500 sq. meter office floor in CBD Towers. This included a complete overhaul of the interior layout to create open-plan workspaces, new meeting rooms, and a modern kitchenette. Our team handled all aspects of the renovation, including new electrical wiring for enhanced data and power access, installation of energy-efficient LED lighting, and upgrading the plumbing systems for the new kitchen and restrooms. The project was completed on schedule, delivering a vibrant and highly functional modern workspace.",
        images: [
            'https://media.gettyimages.com/id/1329335836/photo/office-interior.jpg?s=612x612&w=0&k=20&c=7IC3a4lDlGCxucQ2sk3wXsN9Nl5brDG3odBuuhLkkag=',
            'https://media.gettyimages.com/id/2219657920/photo/modern-office-interior-with-white-desks-and-clean-design.jpg?s=612x612&w=0&k=20&c=FMLrbr1p_OU6Lc4S2beptMQjEpiKXQapjcv9OlniFOU=',
            'https://media.gettyimages.com/id/1329335814/photo/interior-of-modern-office-with-empty-desk.jpg?s=612x612&w=0&k=20&c=vkSZ_5i0J8MwWstBkcgR1V6EU2ybzjYhOTJqPvdqRGM=',
            'https://media.gettyimages.com/id/1329335879/photo/modern-office-interior.jpg?s=612x612&w=0&k=20&c=MfrRu0v7OXVx5o5nui-kvM2u0hsOHQwfWI0-sd-e-bs=',
        ]
    },
    {
        "title": "Residential Villa Construction - Runda Estate",
        "desc": "We successfully completed the construction of a luxurious 5-bedroom residential villa in the prestigious Runda Estate. From groundbreaking to final finishes, Walrish Contractors LTD managed the entire construction process. This included laying robust foundations, erecting the structural framework, installing the roof, and executing high-quality finishing works such as bespoke cabinetry, tiling, and painting. Our meticulous project management ensured adherence to design specifications, budget, and timelines, resulting in a beautiful and durable family home.",
        images: [
            'https://img.freepik.com/premium-photo/house-construction-with-autoclaved-aerated-concrete-block-structure-building-site_293060-1533.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740',
            'https://img.freepik.com/premium-photo/new-residential-house-contemporary-style-building-progress-construction-site-with-blue-sky_293060-395.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740',
            'https://img.freepik.com/premium-photo/house-construction-with-autoclaved-aerated-concrete-block-structure-building-site_293060-3280.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740',
            'https://img.freepik.com/premium-photo/interior-new-house-architectural-residential-construction-home_73110-4864.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740'
        ]
    },
    {
        "title": "School Building Rehabilitation & Accessibility Upgrade - Greenhill Academy",
        "desc": "Walrish Contractors LTD was contracted to rehabilitate an aging classroom block at Greenhill Academy. The project involved extensive structural repairs, roof replacement, and general building maintenance to ensure a safe learning environment. A key component of this project was the implementation of accessibility upgrades, including the installation of ramps and accessible restroom facilities, to ensure the building was inclusive for all students. The rehabilitation significantly extended the lifespan of the building and improved its functionality.",
        images: [
            'https://img.freepik.com/premium-photo/group-people-are-walking-around-garden-with-roof-that-says-word-it_517312-46521.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740',
            'https://media.gettyimages.com/id/1414877372/photo/empty-classroom-with-rows-of-desks-at-a-community-college.jpg?s=612x612&w=0&k=20&c=d-9ZwLICuJ_MKPlAlWy4OACr2-Na0PZ6-e0-yHbeFs8=',
            'https://img.freepik.com/premium-photo/hotel-walkway-with-light-flare_91566-753.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740',
            'https://media.gettyimages.com/id/1134800464/photo/male-bathroom-of-a-school.jpg?s=612x612&w=0&k=20&c=kL1rhkSr61pIl5VMTni-4y-E8URlLwpuEIcHCEM2A7w='
        ]
    },
    {
        "title": "Industrial Warehouse Electrical & Plumbing Upgrade - Athi River EPZ",
        "desc": "For a major logistics company in the Athi River EPZ, Walrish Contractors LTD executed a critical electrical and plumbing upgrade for their 2,000 sq. meter warehouse. This involved upgrading the entire electrical distribution system to accommodate new machinery, installing heavy-duty lighting, and overhauling the fire suppression plumbing lines. We also installed new water and drainage systems for the staff facilities. Our expertise ensured minimal disruption to the client's operations while delivering a robust and compliant infrastructure.",
        images: [
            'https://media.gettyimages.com/id/1323471297/photo/bare-ceiling-with-air-duct-cctv-air-conditioner-pipe-and-fire-sprinkler-system-on-white.jpg?s=612x612&w=0&k=20&c=Hat_z4PpX6Rq-fB5KLqWff0pF-Upp3Wp734ruaaWV8E=',
            'https://media.gettyimages.com/id/1267456810/photo/human-hand-measuring-ampere-with-meter.jpg?s=612x612&w=0&k=20&c=oXcFDbS9C_dRM9jJthgHo5VAFykdfn3t_FHEALf6TPc=',
            'https://img.freepik.com/premium-photo/male-worker-painted-gray-pipeline-oil-flowing-valve_478515-2789.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740',
            'https://img.freepik.com/premium-photo/closeup-african-plumber-showing-one-dirty-one-clean-filters-changing-water-filters_404612-2338.jpg?uid=R159964388&ga=GA1.1.921452864.1748509657&semt=ais_items_boosted&w=740',
        ]
    }
])
let image = ref(0)
let id = ref(0)
onMounted(() => {
    projects.value.forEach((el, index) => {
        if (el.title == useRoute().params.id.replaceAll('_', ' ')) {
            id.value = index;
        }
    })
    setInterval(() => {
        if (image.value == 3) {
            image.value = 0
            return
        }
        image.value++
    }, 5000)
})
</script>