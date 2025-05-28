<template>
  <!-- <main class="bg-[#202026] h-screen pt-10">
   <Hero class="text-white"></Hero>
  </main> -->
  <main>
    <Hero2 id=""/>
    <About id="about_us"/>
    <Services id="services"/>
    <Statistics/>
    <Testimonials/>
    <Footer id="contacts"/>
  </main>
</template>

<script setup>
useHead({
  title: 'Walrish Contractors',
  meta: [
    {
      name: 'description',
      content: 'Walrish Contractors is a leading construction company specializing in residential and commercial projects. We are committed to delivering high-quality construction services with a focus on safety, sustainability, and customer satisfaction.'
    }
  ]
})
useSeoMeta({
  title: 'Walrish Contractors',
  description: 'Leading construction company specializing in residential and commercial projects. We are committed to delivering high-quality construction services with a focus on safety, sustainability, and customer satisfaction.',
  image: 'https://img.freepik.com/free-photo/building-new-concrete-house_1398-2995.jpg?uid=R159964388&ga=GA1.1.825660883.1729923843&semt=ais_hybrid&w=740',
  url: 'https://walrish-contractors.com'
})
useSeoMeta({
  ogTitle: 'Warlish Contractors',
  ogDescription: 'Leasding construction company specializing in residential and commercial projects. We are committed to delivering high-quality construction services with a focus on safety, sustainability, and customer satisfaction.',
  ogImage: '/image.png',
  ogUrl: 'https://walrish-contractors.com',
  twitterTitle: 'Walrish Contractors - twitter',
  twitterDescription: '[twitter:description]',
  twitterImage: '[twitter:image]',
  twitterCard: 'summary',
  facebookTitle: '[facebook:title]',
  facebookDescription: '[facebook:description]',
  facebookImage: '/image.png',
  facebookUrl: '[facebook:url]',
})

useHead({
  htmlAttrs: {
    lang: 'en'
  },
  link: [
    {
      rel: 'icon',
      type: 'image/png',
      href: '/favicon.png'
    }
  ]
})
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Cinzel+Decorative:wght@400;700;900&family=Cinzel:wght@400..900&family=Jost:ital,wght@0,100..900;1,100..900&family=Lora:ital,wght@0,400..700;1,400..700&display=swap');
.cinzel-400 {
  font-family: "Cinzel Decorative", serif;
  font-weight: 400;
  font-style: normal;
}

.cinzel-700 {
  font-family: "Cinzel Decorative", serif;
  font-weight: 700;
  font-style: normal;
}

.cinzel-900 {
  font-family: "Cinzel Decorative", serif;
  font-weight: 900;
  font-style: normal;
}

.cinzel-500 {
  font-family: "Cinzel", serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
}
.lora-500 {
  font-family: "Lora", serif;
  font-optical-sizing: auto;
  font-weight:500;
  font-style: normal;
}
.lora-400 {
  font-family: "Lora", serif;
  font-optical-sizing: auto;
  font-weight:400;
  font-style:italic;
}
.jost-500 {
  font-family: "Jost", sans-serif;
  font-optical-sizing: auto;
  font-weight: 500;
  font-style: normal;
}
.jost-900 {
  font-family: "Jost", sans-serif;
  font-optical-sizing: auto;
  font-weight: 900;
  font-style: normal;
}

</style>