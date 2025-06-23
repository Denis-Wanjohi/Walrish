<template>
    <div class="bg-black hide-scrollbar">
        <Hero2 id=""/>
    <Services id="services" class="pt-20"/>
    <About id="about_us" class="pt-20"/>
    <Statistics/>
    <Projects id="projects" class="bg-black"/>
    <Testimonials id="testimonials"/>
    <ContactForm id="contacts" class="pt-20"/>
    <Footer id="footer"/>
    </div>
</template> 

<script setup>
definePageMeta({ssr:false})
onMounted(()=>{
    if(useRoute().fullPath.includes("section")){
        let section = useRoute().query.section
        useRouter().push('/#'+section)
    }
})
</script>