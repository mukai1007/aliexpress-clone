<script setup>
import MainLayout from '~/layouts/MainLayout.vue';

</script>
<template>
    <MainLayout>
        <div id="ShoppingCartPage" class="mt-4 max-w-[1200px] mx-auto px-2">
            <div v-if="false" class="h-[500px] flex items-center justify-center">
                <div class="pt-20">
                    <img 
                        class="mx-auto"
                        width="250"
                        src="../public/cart-empty.png"
                    >

                    <div class="text-xl text-center mt-4">No items yet?</div>

                    <div v-if="!user" class="flex text-center">
                        <NuxtLink 
                            to="/auth"
                            class="
                                bg-[#FD374F] 
                                w-full 
                                text-white 
                                text-[21px] 
                                font-semibold 
                                p-1.5 
                                rounded-full
                                mt-4
                            "
                        >
                            Sign in
                        </NuxtLink>
                    </div>
                </div>
            </div>

            <div v-else class="md:flex gap-4 justify-between mx-auto w-full">
                <div class="md:w-[65%]">
                    <div class="bg-white rounded-lg p-4">
                        <div class="text-2xl font-bold mb-2">
                            Shopping Cart (0)
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </MainLayout>
</template>
