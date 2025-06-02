<template>
    <form class="border-b  px-2 border-gray-200/10 pb-12 sm:w-5/12 mx-auto bg-black text-white" @submit.prevent="submitted">
        <h2 class=" text-2xl text-center pt-5 font-bold sm:text-4xl leading-7 py-2 text-gray-200">Contact Form</h2>
        <p class="mt-1 text-sm  text-center leading-6 text-gray-400">Incase of any inquiry please reach out to us through this
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
                <label for="first-name" class="block text-sm font-semibold leading-6 text-gray-200">Email</label>
                <div class="mt-2">
                    <input type="text" required v-model="user.name" name="first-name" id="first-name"
                        autocomplete="given-name"
                        class="block w-full px-4    rounded-md border-0 py-1.5 text-gray-200 shadow-sm ring-1 ring-inset ring-gray-300 placeholder:text-gray-400  sm:text-sm sm:leading-6">
                </div>
            </div>
            <!-- PHONE -->
            <div class="sm:col-span-3">
                <label for="first-name" class="block text-sm font-semibold leading-6 text-gray-200">Phone Number</label>
                <div class="mt-2">
                    <input type="text" required v-model="user.phone" name="first-name" id="first-name"
                        autocomplete="given-name"
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
            <button class="py-3 bg-blue-400 hover:bg-blue-500 cursor-pointer  rounded-md sm:col-span-6 w-3/4 font-semibold mx-auto" type="submit">
            Submit
            </button>
        </div>
    </form>

</template>

<script setup>
const user = ref({
    name: null,
    email: null,
    phone: null,
    message: null,
})
function submitted(){
    console.log(user.value)
}
</script>