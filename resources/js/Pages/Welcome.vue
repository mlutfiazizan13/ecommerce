<script setup>
import WebLayout from '@/Layouts/WebLayout.vue';
import { Head, Link } from '@inertiajs/vue3';
import Glide from '@glidejs/glide';
import { onMounted } from 'vue';
import ProductCard from '@/Components/ProductCard.vue';

onMounted(() => {
    const glide = new Glide('.glide',  {
        type: 'carousel',
        startAt: 0,
        gap: 0
    }).mount();
})
 

</script>

<template>

    <!-- <div class="relative sm:flex sm:justify-center sm:items-center min-h-screen bg-dots-darker bg-center bg-gray-100 dark:bg-dots-lighter dark:bg-gray-900 selection:bg-red-500 selection:text-white">
        <div v-if="canLogin" class="sm:fixed sm:top-0 sm:end-0 p-6 text-end z-10">
            <Link v-if="$page.props.auth.user" :href="route('dashboard')" class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500">Dashboard</Link>

            <template v-else>
                <Link :href="route('login')" class="font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500">Log in</Link>

                <Link v-if="canRegister" :href="route('register')" class="ms-4 font-semibold text-gray-600 hover:text-gray-900 dark:text-gray-400 dark:hover:text-white focus:outline focus:outline-2 focus:rounded-sm focus:outline-red-500">Register</Link>
            </template>
        </div>
    </div> -->

    <WebLayout title="Home">
    
        <section class="">
            <div class="glide">
                <div class="glide__track" data-glide-el="track">
                  <ul class="glide__slides">
                    <li class="glide__slide ml-0 mr-0">
                        <div class="flex justify-center items-center bg-vintage h-[890px] cursor-default">
                            <div class="relative max-w-[1200px] mx-auto">
                                <div class=" grid grid-cols-2 gap-10 items-center">
                                    <div class="w-full text-light-black">
                                        <p class="text-lg uppercase font-bold">New Product!</p>
                                        <p class="text-8xl font-medium mb-10">PRODUCT</p>
                                        <p class="text-sm opacity-70 mb-10">Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque at cum provident, perspiciatis aspernatur incidunt repudiandae? Ducimus tempore vitae itaque.</p>
                                        <a href="#" class="bg-lighter-black text-white py-2 px-5 text-lg">Check Now !</a>
                                    </div>
                                    <div>
                                        <img src="https://htmldemo.net/payne/payne/assets/img/slider/slider-image-02.png" alt="">
                                    </div>
                                </div>

                            </div>
                           
                        </div>
                    </li>
                    <li class="glide__slide ml-0 mr-0">    
                        <div class=" flex justify-center items-center bg-vintage h-[890px] cursor-default">
                            <div class="relative max-w-[1200px] mx-auto">
                                <div class=" grid grid-cols-2 gap-10 items-center">
                                    <div class="w-full text-light-black">
                                        <p class="text-lg uppercase font-bold">New Product!</p>
                                        <p class="text-8xl font-medium mb-10">PRODUCT</p>
                                        <p class="text-sm opacity-70 mb-10">Lorem ipsum dolor sit amet consectetur adipisicing elit. Atque at cum provident, perspiciatis aspernatur incidunt repudiandae? Ducimus tempore vitae itaque.</p>
                                        <a href="#" class="bg-lighter-black text-white py-2 px-5 text-lg">Check Now !</a>
                                    </div>
                                    <div>
                                        <img src="https://www.newbalance.co.id/media/catalog/product/cache/c1feb3550df60acd013ba17bf29e4991/0/8/0888-NEWMT580ADBGRE10H-1.jpg" alt="">
                                    </div>
                                </div>

                            </div>
                           
                        </div>
                    </li>
                  </ul>
                </div>
                <div class="glide__bullets" data-glide-el="controls[nav]">
                    <button class="glide__bullet border " data-glide-dir="=0"></button>
                    <button class="glide__bullet border " data-glide-dir="=1"></button>
                  </div>
              </div>
        </section>


        <section class="relative max-w-[1200px] mx-auto py-20">
            <div class="text-center">
                <p class="text-5xl font-medium mb-3">Our Latest Arrival</p>
                <p class="text-sm opacity-70">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Exercitationem, cumque?</p>
            </div>
            <div class="grid grid-cols-3 gap-3 py-20">
                <div>
                    <div class="h-[500px] w-full bg-light-black">

                    </div>
                    
                </div>
                <div>
                    <div class="h-[500px] w-full bg-light-black">

                    </div>
                    
                </div>
                <div>
                    <div class="h-[500px] w-full bg-light-black">

                    </div>
                    
                </div>

            </div>
        </section>

        <section class="relative max-w-[1200px] mx-auto py-20">
            <div class="text-center">
                <p class="text-5xl font-medium mb-3">Our Products</p>
                <p class="text-sm opacity-70">Lorem ipsum, dolor sit amet consectetur adipisicing elit. Exercitationem, cumque?</p>
            </div>
            <div class="grid grid-cols-3 gap-3 py-20">
                <ProductCard 
                    image="https://www.newbalance.co.id/media/catalog/product/cache/c1feb3550df60acd013ba17bf29e4991/0/8/0888-NEWMT580ADBGRE10H-1.jpg"
                    title="Lorem Ipsum"
                    price="2.000.000" />

                <ProductCard 
                    image="https://www.newbalance.co.id/media/catalog/product/cache/c1feb3550df60acd013ba17bf29e4991/0/8/0888-NEWMT580ADBGRE10H-1.jpg"
                    title="Lorem Ipsum"
                    price="2.000.000" />

                <ProductCard 
                    image="https://www.newbalance.co.id/media/catalog/product/cache/c1feb3550df60acd013ba17bf29e4991/0/8/0888-NEWMT580ADBGRE10H-1.jpg"
                    title="Lorem Ipsum"
                    price="2.000.000" />

                <ProductCard 
                    image="https://www.newbalance.co.id/media/catalog/product/cache/c1feb3550df60acd013ba17bf29e4991/0/8/0888-NEWMT580ADBGRE10H-1.jpg"
                    title="Lorem Ipsum"
                    price="2.000.000" />

                <ProductCard 
                    image="https://www.newbalance.co.id/media/catalog/product/cache/c1feb3550df60acd013ba17bf29e4991/0/8/0888-NEWMT580ADBGRE10H-1.jpg"
                    title="Lorem Ipsum"
                    price="2.000.000" />

                <ProductCard 
                    image="https://www.newbalance.co.id/media/catalog/product/cache/c1feb3550df60acd013ba17bf29e4991/0/8/0888-NEWMT580ADBGRE10H-1.jpg"
                    title="Lorem Ipsum"
                    price="2.000.000" />
                

                
                

            </div>
        </section>
    </WebLayout>

</template>
