<script setup>
import { computed } from 'vue';
import { Link } from '@inertiajs/vue3';
import { FontAwesomeIcon } from '@fortawesome/vue-fontawesome'
import { faEnvelope } from '@fortawesome/free-solid-svg-icons'

// const props = defineProps({
//     href: String,
//     active: Boolean,
// });

// const classes = computed(() => {
//     return props.active
//         ? 'inline-flex items-center px-1 pt-1 border-b-2 border-indigo-400 text-sm font-medium leading-5 text-gray-900 focus:outline-none focus:border-indigo-700 transition duration-150 ease-in-out'
//         : 'inline-flex items-center px-1 pt-1 border-b-2 border-transparent text-sm font-medium leading-5 text-gray-500 hover:text-gray-700 hover:border-gray-300 focus:outline-none focus:text-gray-700 focus:border-gray-300 transition duration-150 ease-in-out';
// });
</script>

<template>
    <div class="relative max-w-[1200px] mx-auto">
        <div class="absolute flex justify-between items-center bg-transparent w-full h-[100px] z-50">
            <div class="">
                <p class="text-3xl font-medium">Product</p>
            </div>
            <div class="flex gap-10 text-lg">
                <p>Home</p>
                <p>Producs</p>
                <p>Contact Us</p>
          
            </div>
            <div class="flex gap-5">
                <div class="text-xl">
                    <p>Login</p>
                </div>
                <div class="text-2xl">
                    <font-awesome-icon :icon="['fas', 'heart']" />
                </div>
                <div class="text-2xl">
                    <font-awesome-icon :icon="['fas', 'bag-shopping']" />
                </div>
            </div>
        </div>
    </div>

</template>
