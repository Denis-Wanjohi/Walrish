<template>
    <form class="border-b  px-2 border-gray-200/10 pb-12 sm:w-5/12 mx-auto bg-black text-white"
        @submit.prevent="submitted">
        <h2 class=" text-2xl text-center pt-5 font-bold sm:text-4xl leading-7 py-2 text-gray-200">Contact Form</h2>
        <p class="mt-1 text-sm  text-center leading-6 text-gray-400">Incase of any inquiry please reach out to us
            through this
            form.Thank you :)</p>
        <p class="mt-1 text-sm leading-6 text-center text-gray-400">Please fill in correct details*</p>

        <div class="mt-10  grid grid-cols-1 gap-x-6 gap-y-8 sm:grid-cols-6">
            <!--  NAME -->
            <div class="sm:col-span-3">
                <label for="first-name" class="block text-sm font-semibold leading-6 text-gray-200">Fullname</label>
                <div class="mt-2">
                    <input type="text" required v-model="user.name" name="first-name" id="first-name"
                        autocomplete="given-name"
                        class="block w-full px-4    rounded-md border-0 py-1.5 text-gray-200 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400  sm:text-sm sm:leading-6">
                </div>
            </div>
            <!-- EMAIL -->
            <div class="sm:col-span-3">
                <label for="email" class="block text-sm font-semibold leading-6 text-gray-200">Email</label>
                <div class="mt-2">
                    <input type="email" required v-model="user.email" name="email" id="email" autocomplete="given-name"
                        class="block w-full px-4    rounded-md border-0 py-1.5 text-gray-200 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400  sm:text-sm sm:leading-6">
                </div>
            </div>
            <!-- PHONE -->
            <div class="sm:col-span-3">
                <label for="phone" class="block text-sm font-semibold leading-6 text-gray-200">Phone Number</label>
                <div class="mt-2">
                    <input type="text" required v-model="user.phone" name="phone" id="phone" autocomplete="given-name"
                        class="block w-full px-4    rounded-md border-0 py-1.5 text-gray-200 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400  sm:text-sm sm:leading-6">
                </div>
            </div>
            <!-- MESSAGE -->
            <div class="sm:col-span-6">
                <label for="message" class="block text-sm font-semibold leading-6 text-gray-200">Message</label>
                <div class="mt-2.5">
                    <textarea name="message" placeholder="write something here..." required v-model="user.message"
                        id="message" rows="4" style="max-height: 100px;min-height: 50px;"
                        class="block w-full   rounded-md border-0 px-3.5 py-2  text-gray-200 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400  sm:text-sm sm:leading-6"></textarea>
                </div>
            </div>
            <button v-if="!submitting && !submittedSuccess && !submitError"
                class="py-3 bg-blue-400 hover:bg-blue-500 cursor-pointer  rounded-md sm:col-span-6 w-3/4 font-semibold mx-auto"
                type="submit">
                Submit <i class="pi-plus"></i>
            </button>
            <div class="py-3 bg-blue-400 hover:bg-blue-500 cursor-pointer  rounded-md sm:col-span-6 w-3/4 font-semibold mx-auto flex justify-center"
                v-if="submitting">
                <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24">
                    <circle cx="12" cy="2" r="0" fill="currentColor">
                        <animate attributeName="r" begin="0" calcMode="spline" dur="1.3s"
                            keySplines="0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8" repeatCount="indefinite"
                            values="0;2;0;0" />
                    </circle>
                    <circle cx="12" cy="2" r="0" fill="currentColor" transform="rotate(45 12 12)">
                        <animate attributeName="r" begin="0.163s" calcMode="spline" dur="1.3s"
                            keySplines="0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8" repeatCount="indefinite"
                            values="0;2;0;0" />
                    </circle>
                    <circle cx="12" cy="2" r="0" fill="currentColor" transform="rotate(90 12 12)">
                        <animate attributeName="r" begin="0.325s" calcMode="spline" dur="1.3s"
                            keySplines="0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8" repeatCount="indefinite"
                            values="0;2;0;0" />
                    </circle>
                    <circle cx="12" cy="2" r="0" fill="currentColor" transform="rotate(135 12 12)">
                        <animate attributeName="r" begin="0.488s" calcMode="spline" dur="1.3s"
                            keySplines="0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8" repeatCount="indefinite"
                            values="0;2;0;0" />
                    </circle>
                    <circle cx="12" cy="2" r="0" fill="currentColor" transform="rotate(180 12 12)">
                        <animate attributeName="r" begin="0.65s" calcMode="spline" dur="1.3s"
                            keySplines="0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8" repeatCount="indefinite"
                            values="0;2;0;0" />
                    </circle>
                    <circle cx="12" cy="2" r="0" fill="currentColor" transform="rotate(225 12 12)">
                        <animate attributeName="r" begin="0.813s" calcMode="spline" dur="1.3s"
                            keySplines="0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8" repeatCount="indefinite"
                            values="0;2;0;0" />
                    </circle>
                    <circle cx="12" cy="2" r="0" fill="currentColor" transform="rotate(270 12 12)">
                        <animate attributeName="r" begin="0.975s" calcMode="spline" dur="1.3s"
                            keySplines="0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8" repeatCount="indefinite"
                            values="0;2;0;0" />
                    </circle>
                    <circle cx="12" cy="2" r="0" fill="currentColor" transform="rotate(315 12 12)">
                        <animate attributeName="r" begin="1.137s" calcMode="spline" dur="1.3s"
                            keySplines="0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8;0.2 0.2 0.4 0.8" repeatCount="indefinite"
                            values="0;2;0;0" />
                    </circle>
                </svg>
            </div>
            <div v-if="submittedSuccess"
                class="py-3 bg-green-400 hover:bg-green-500 cursor-pointer  rounded-md sm:col-span-6 w-3/4 font-semibold mx-auto  text-center">
                S E N T !</div>
            <div v-if="submitError"
                class="py-3 bg-red-400 hover:bg-red-500 cursor-pointer  rounded-md sm:col-span-6 w-3/4 font-semibold mx-auto  text-center">
                NOT SENT. RETRY!</div>
        </div>
    </form>

</template>

<script setup>
const submitting = ref(false)
const submittedSuccess = ref(false)
const submitError = ref(false)
const user = ref({
    name: null,
    email: null,
    phone: null,
    message: null,
})
async function submitted() {
    submitting.value = true
    console.log(user.value)
    const res = await $fetch(' http://localhost:3001/message', {
        method: 'POST',
        body: {
            data: user.value
        }
    })
        .catch(err => {
            submitting.value = false
            submitError.value = true
            setTimeout(() => {
                submitError.value = false
                submitting.value = false

            }, 4000);
            return
        })

    if (res.message == "Email sent successfully") {
        user.value.email = null
        user.value.name = null
        user.value.message = null
        user.value.phone = null
        submitting.value = false
        submittedSuccess.value = true
        setTimeout(() => {
            submittedSuccess.value = false
        }, 4000);
    }


}
</script>
<!-- ghghhg -->
<!-- fetch('https://fakestoreapi.com/products', {
    method: 'POST',
    headers: { 'Content-Type': 'application/json' },
    body: JSON.stringify(data)
})
    .then(response => response.json())
    .then(result => console.log(result)); -->