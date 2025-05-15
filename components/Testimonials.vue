<template>
    <div class="py-5 bg-black text-white">
        <div class="text-center font-bold sm:text-5xl text-3xl shadow-sm py-3 mx-auto">
            Our clients say
        </div>


        <div class="overflow-x-auto hide-scrollbar">
            <div class="flex space-x-4">
                <div class="min-w-[400px] shadow-md rounded-lg p-6" data-aos="zoom-in"  v-for="(testimony,i) in testimonials" :key="i">
                    <div style="" class="h-[200px]  cursor-pointer lora-400 rounded-xl border  overflow-y-auto hide-scrollbar pt-5 px-3 text-md ">
                        {{ testimony.testimony }}
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script  setup>

const testimonials = [
  {
    "testimony": "We entrusted Walrish with our new commercial building project, and we couldn't be happier with the results. Their project management was excellent, the quality of construction was top-notch, and they delivered on time. A reliable and professional team!",
    "name": "Sarah Miller",
    "profession": "CEO, Tech Solutions Inc."
  },
  {
    "testimony": "When we had a major plumbing emergency, Walrish Contractors responded quickly and efficiently. Their plumber expertly diagnosed and repaired the issue, preventing further damage. Their prompt service saved us a lot of stress and money.",
    "name": "David Omondi",
    "profession": "Restaurant Owner"
  },
  {
    "testimony": "The electrical work done by Walrish in our home renovation was outstanding. They installed new lighting fixtures and upgraded our outlets with precision and care. The electricians were knowledgeable and ensured everything was up to code. Highly recommend!",
    "name": "Jane Wanjiku",
    "profession": "Homemaker"
  },
  {
    "testimony": "Our building needed significant repairs, and Walrish Contractors provided a thorough and effective solution. From fixing structural issues to repainting, their team was skilled and meticulous. The building looks and feels as good as new.",
    "name": "Michael Kariuki",
    "profession": "Property Manager"
  },
  {
    "testimony": "Walrish Contractors completely transformed our living space with their interior renovation service. They listened to our ideas, offered creative solutions, and the final result is beyond our expectations. The attention to detail and quality of workmanship were fantastic.",
    "name": "Emily Akinyi",
    "profession": "Marketing Executive"
  },
  {
    "testimony": "We engaged Walrish for some civil engineering works on our property, including drainage construction. Their team was professional, efficient, and the work was completed to a high standard. We were impressed with their expertise and attention to detail.",
    "name": "John Kamau",
    "profession": "Land Developer"
  }
]
</script>

<style>
/* Hide scrollbar for Chrome, Safari and Opera */
.hide-scrollbar::-webkit-scrollbar {
  display: none;
}

/* Hide scrollbar for IE, Edge, and Firefox */
.hide-scrollbar {
  -ms-overflow-style: none; /* IE and Edge */
  scrollbar-width: none; /* Firefox */
}

</style>