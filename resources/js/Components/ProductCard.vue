<script setup>
defineProps({
    image: String,
    title: String,
    price: Number,
    discount: Number,
});
</script>

<template>
    <div class="w-full bg-gray shadow-md border border-gray">
        <img :src="image" alt="">
        <div class="p-5">
            <p class="font-medium text-lg mb-2">{{title}}</p>
            <p class="font-medium">Rp {{price}}</p>
        </div>
    </div>
</template>
