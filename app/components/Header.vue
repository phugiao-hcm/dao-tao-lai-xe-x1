<template>
    <header class="bg-white shadow sticky top-0 z-50">
        <div
            class="max-w-7xl mx-auto px-4 py-3 flex items-center justify-between"
        >
            <NuxtLink to="/" class="font-bold text-xl"
                >Lái xe Phú Giáo</NuxtLink
            >
            <nav class="hidden md:flex space-x-6 text-gray-700">
                <NuxtLink to="/" class="hover:text-blue-600"
                    >Trang chủ</NuxtLink
                >
                <NuxtLink to="#courses" class="hover:text-blue-600"
                    >Khóa học</NuxtLink
                >
                <NuxtLink to="#team" class="hover:text-blue-600"
                    >Đội ngũ</NuxtLink
                >
                <NuxtLink to="#contact" class="hover:text-blue-600"
                    >Liên hệ</NuxtLink
                >
            </nav>
            <button @click="open = !open" class="md:hidden text-gray-700">
                <span v-if="!open">☰</span><span v-else>✕</span>
            </button>
        </div>
        <div v-if="open" class="md:hidden bg-white px-4 space-y-2 pb-4">
            <NuxtLink to="/" class="block py-1">Trang chủ</NuxtLink>
            <NuxtLink to="#courses" class="block py-1">Khóa học</NuxtLink>
            <NuxtLink to="#team" class="block py-1">Đội ngũ</NuxtLink>
            <NuxtLink to="#contact" class="block py-1">Liên hệ</NuxtLink>
        </div>
    </header>
</template>

<script setup>
import { ref } from "vue";
const open = ref(false);
</script>
