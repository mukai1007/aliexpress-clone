<script setup>
import MainLayout from '../layouts/MainLayout.vue';
import { useUserStore } from '~/stores/user';
import { ref } from 'vue';
const userStore = useUserStore()

const products = ref(null)
onBeforeMount( async () => {
    products.value = await useFetch('/api/prisma/get-all-products')
    setTimeout(() => userStore.isLoading = false, 1000)
})
// const products = [
//     {id: 1, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/237/800/800', price: 1234},
//     {id: 2, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/238/800/800', price: 1234},
//     {id: 3, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/239/800/800', price: 1234},
//     {id: 4, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/240/800/800', price: 1234},
//     {id: 5, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/241/800/800', price: 1234},
//     {id: 6, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/242/800/800', price: 1234},
//     {id: 7, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/243/800/800', price: 1234},
//     {id: 8, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/244/800/800', price: 1234},
//     {id: 9, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/235/800/800', price: 1234},
//     {id: 10, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/236/800/800', price: 1234},
//     {id: 11, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/247/800/800', price: 1234},
//     {id: 12, title: 'title 1', description: 'this is a description', url: 'https://picsum.photos/id/248/800/800', price: 1234},
// ]

</script>

<template>
    <MainLayout>
        <div id="IndexPage" class="mt-4 max-w-[1200px] mx-auto px-2">
            <div class="grid xl:grid-cols-6 lg:grid-cols-5 md:grid-cols-4 sm:grid-cols-3 grid-cols-2 gap-4">
                <div v-if="products" v-for="product in products.data" :key="product">
                    <ProductItem :product="product"/>
                </div>
            </div>
        </div>
    </MainLayout>
</template>