<script setup>
import MainLayout from '../layouts/MainLayout.vue';
const products = [
    {id: 1, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/237/200/300', price: 1234},
    {id: 2, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/238/200/300', price: 1234},
    {id: 3, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/239/200/300', price: 1234},
    {id: 4, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/240/200/300', price: 1234},
    {id: 5, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/241/200/300', price: 1234},
    {id: 6, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/242/200/300', price: 1234},
    {id: 7, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/243/200/300', price: 1234},
    {id: 8, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/244/200/300', price: 1234},
    {id: 9, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/235/200/300', price: 1234},
    {id: 10, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/236/200/300', price: 1234},
    {id: 11, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/247/200/300', price: 1234},
    {id: 12, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/248/200/300', price: 1234},
]

</script>

<template>
    <MainLayout>
        <div id="IndexPage" class="mt-4 max-w-[1200px] mx-auto px-2">
            <div class="grid xl:grid-cols-6 lg:grid-cols-5 md:grid-cols-4 sm:grid-cols-3 grid-cols-2 gap-4">
                <div v-if="products" v-for="product in products" :key="product">
                    <ProductItem :product="product"/>
                </div>
            </div>
        </div>
    </MainLayout>
</template>