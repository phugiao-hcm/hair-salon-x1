<template>
    <header class="bg-white shadow-md sticky top-0 z-50">
        <div class="max-w-7xl mx-auto flex justify-between items-center p-4">
            <NuxtLink to="/" class="text-2xl font-bold text-gray-800"
                >Salon Phú Giáo</NuxtLink
            >
            <button @click="open = !open" class="md:hidden text-gray-700">
                <span v-if="!open">☰</span><span v-else>✕</span>
            </button>

            <nav class="hidden md:flex space-x-6 text-gray-700">
                <NuxtLink to="#home">Trang chủ</NuxtLink>
                <NuxtLink to="#services">Dịch vụ</NuxtLink>
                <NuxtLink to="#portfolio">Portfolio</NuxtLink>
                <NuxtLink to="#booking">Đặt lịch</NuxtLink>
            </nav>
        </div>
        <div v-if="open" class="md:hidden bg-white p-4 space-y-2">
            <NuxtLink to="#home" class="block">Trang chủ</NuxtLink>
            <NuxtLink to="#services" class="block">Dịch vụ</NuxtLink>
            <NuxtLink to="#portfolio" class="block">Portfolio</NuxtLink>
            <NuxtLink to="#booking" class="block">Đặt lịch</NuxtLink>
        </div>
    </header>
</template>
<script setup>
import { ref } from "vue";
const open = ref(false);
</script>
