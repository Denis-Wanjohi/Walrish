<template>
    <div class="w-11/12   bg-black text-white overflow-hidden pb-20 lg:pb-10">
        <h2 class=" lg:text-[100px] md:text-[70px] text-[50px] jost-900 text-white  absolute lg:left-[30%] left-[10%] animate__animated animate__fadeInDown ">Our Services</h2>
        <div class="md:mt-0 mt-20"></div>
        <div  v-for="(service, index) in w_services" :key="index">
            <div class="md:flex "  :class="[index % 2 == 1 ? 'flex-row-reverse lg:p-20 p-2' : '']" >
                <div class="md:w-1/2 md:pl-10 pl-5 md:mt-30">
                <h3 class="cinzel-700 text-center sm:text-2xl text-xl text-[#FFA500]"  data-aos="flip-up">{{service.title}}</h3>
                <p class="lora-500 sm:text-md text-sm leading-6 lg:pr-20">{{ service.description }}</p>
                <div class="mt-2" v-for="(s, index) in service.services" :key="index">
                    <p class="text-slate-300"> - {{ s }}</p>
                </div>
            </div>
            <div class="md:w-1/2  w-screen md:mt-40 mt-3">
                <img :src=" service.image_1 "
                    alt="walrish_contractors" class="lg:w-1/2 md:3/4 w-screen md:h-[120%]   object-cover " data-aos="zoom-in">
                <img :src=" service.image_2 "
                    alt="walrish_contractors" class="w-[60%] md:h-[80%] h-[100%] relative object-cover md:left-[30%] left-[30%] md:-top-[80%] bottom-[100%]  " data-aos="flip-right">
            </div>
            </div>
        </div>
    </div>
</template>

<script setup>
import AOS from 'aos'
import 'aos/dist/aos.css'
onMounted(() => {
    AOS.init({
        duration: 1000,
        easing: 'ease-in-out',
        once: true,
    });
});
const w_services = [
    {
        title: "General construction",
        description: "We provide reliable construction services focused on quality, safety, and timely delivery transforming concepts into durable, functional structures.",
        image_1: "https://img.freepik.com/free-photo/construction-site_53876-23128.jpg?t=st=1747301766~exp=1747305366~hmac=d531011d1564b94257614207823745b1228dac7851ce062eb12001fd36e0f4a9&w=826",
        image_2: "https://img.freepik.com/free-photo/beautiful-view-construction-site-city-sunset_181624-9347.jpg?uid=R159964388&ga=GA1.1.825660883.1729923843&semt=ais_hybrid&w=740",
        services: [
            "Residential Construction",
            "Commercial Building Projects",
            "Civil Engineering Works",
            "Renovations and Remodeling",
            "Project Management",
            "Site Preparation and Earthworks",
            "Structural and Finishing Works",
            "Road and Drainage Construction",
            "Consultancy and Planning Services"
        ],
    },
    {
        title: "Plumbing installation and repairs",
        description: "We offer comprehensive plumbing services, ensuring efficient and reliable water and drainage systems for your property. Our skilled technicians handle everything from new installations to urgent repairs, prioritizing functionality and hygiene.",
        image_1: "https://img.freepik.com/premium-photo/closeup-african-plumber-showing-one-dirty-one-clean-filters-changing-water-filters_404612-2338.jpg?uid=R159964388&ga=GA1.1.825660883.1729923843&semt=ais_hybrid&w=740",
        image_2: "https://img.freepik.com/premium-photo/repairing-clogged-leaky-washbasin-sewer-bathroom_63097-423.jpg?uid=R159964388&ga=GA1.1.825660883.1729923843&semt=ais_hybrid&w=740",
        services: [
            'New Plumbing System Installations',
            'Fixture Installations and Replacements',
            'Pipe Repairs and Leak Detection',
            'Drain Cleaning and Unclogging',
            'Water Heater Installations and Repairs',
            'Sewer Line Inspections and Repairs',
            'Water Tank Installations and Maintenance',
        ],
    },
    {
        title: "Electrical installation and repairs",
        description: "Our certified electricians deliver safe and efficient electrical services, from initial installations to troubleshooting and repairs. We adhere to the highest safety standards to ensure the reliable operation of your electrical systems.",
        image_1: "https://img.freepik.com/premium-photo/free-indian-photo-man-electrical-technician-working-switchboard-with-fuses_937531-17.jpg?uid=R159964388&ga=GA1.1.825660883.1729923843&semt=ais_hybrid&w=740",
        image_2: "https://img.freepik.com/free-photo/man-electrical-technician-working-switchboard-with-fuses-installation-connection-electrical-equipment-close-up_169016-5075.jpg?uid=R159964388&ga=GA1.1.825660883.1729923843&semt=ais_hybrid&w=740",
        services: [
            'New Electrical System Installations',
            'Lighting Installations and Design',
            'Power Outlet and Switch Installations',
            'Electrical Panel Upgrades',
            'Wiring Repairs and Replacements',
            'Appliance Wiring',
            'Emergency Electrical Services',
            'Generator Installations and Maintenance',
        ],
    },
    {
        title: "Building repairs and maintenance",
        description: "We provide comprehensive building repair and maintenance services to keep your property in excellent condition, addressing wear and tear and preventing future issues.",
        image_1: "https://media.gettyimages.com/id/1217394316/photo/application-of-facade-plaster-in-autumn.jpg?s=612x612&w=0&k=20&c=iOsE3FzvQi44bhe9UQNwIIfWMZFnr8EzEbJ4e5cJdZk=",
        image_2: "https://media.gettyimages.com/id/1168410755/photo/workmans-toolbelt-ready-for-building-maintenance-work.jpg?s=612x612&w=0&k=20&c=6jDhp0bEN_e-Z2pkAz1z56-KAvfQDMVyrMCF0-JjDp0=",
        services: [
            'General Building Repairs',
            'Painting and Finishing',
            'Roof Repairs and Maintenance',
            'Plastering and Drywall Repairs',
            'Carpentry and Woodwork Repairs',
            'Floor Repairs and Installations',
            'Preventive Maintenance Programs',
        ],
    },
    {
        title: "Rehabilitations",
        description: "We specialize in the rehabilitation of existing structures, restoring their functionality, safety, and aesthetics. Our approach focuses on preserving the valuable aspects of the building while implementing necessary upgrades.",
        image_1: "https://media.gettyimages.com/id/157192102/photo/three-supervisors-watch-a-scaffolding-worker.jpg?s=612x612&w=0&k=20&c=nbCeDLvez03NxHb1bEU91zxS3jPHxFnByn27Yo9kZOE=",
        image_2: "https://media.gettyimages.com/id/1551534585/photo/mass-of-complex-scaffolding-in-the-city-of-manchester-england.jpg?s=612x612&w=0&k=20&c=v47SWwOJv9fMvmkirGqoYmkAVn2vF9N4gkeTGLVe4lQ=",
        services: [
            'Structural Reinforcements',
            'Restoration of Historical Buildings',
            'Adaptive Reuse of Spaces',
            'Accessibility Improvements',
            'Damage and Water Damage Repairs',
            'Improvement of Energy Efficiency',
        ],
    },
    {
        title: "Renovation",
        description: "Our renovation services focus on transforming and modernizing existing spaces to meet evolving needs and preferences, enhancing both functionality and visual appeal.",
        image_1: "https://media.gettyimages.com/id/1992657656/photo/house-or-apartment-indoor-improvements-and-repairs-works-in-the-very-beginning-construction.jpg?s=612x612&w=0&k=20&c=1WYFdXIuHR9BFmKSyw0SvuCgMJgYQ-kxnW8caQ5NEbg=",
        image_2: "https://media.gettyimages.com/id/155428483/photo/concrete-block-construction-after-stucco-series.jpg?s=612x612&w=0&k=20&c=Lc61yDCq_R_SP5IkmopimuLHfeLwXHJD5nWD4S5PMaQ=",
        services: [
            'Interior Renovations',
            'Exterior Renovations',
            'Kitchen and Bathroom Remodels',
            'Basement Finishing',
            'Room Additions and Extensions',
            'Energy Efficiency Upgrades',
        ],
    }
]
</script>