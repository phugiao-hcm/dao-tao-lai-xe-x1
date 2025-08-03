<template>
    <section class="relative">
        <Swiper
            :modules="[Autoplay, Pagination]"
            :autoplay="{ delay: 4000 }"
            :pagination="{ clickable: true }"
            loop
            class="h-[300px] sm:h-[400px] md:h-[500px] w-full"
        >
            <SwiperSlide v-for="(img, index) in images" :key="index">
                <img
                    :src="img"
                    alt="hero image"
                    class="object-cover w-full h-full"
                />
            </SwiperSlide>
        </Swiper>

        <!-- Text overlay -->
        <div
            class="absolute inset-0 bg-black/40 flex items-center justify-center z-10"
        >
            <div class="text-white text-center space-y-2 px-4">
                <h1 class="text-xl sm:text-2xl md:text-4xl font-bold">
                    Trung tâm đào tạo lái xe Phú Giáo
                </h1>
                <p class="text-sm sm:text-base">
                    Học lái xe ô tô B1, B2, C tại Phú Giáo
                </p>
            </div>
        </div>
    </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";

// Danh sách ảnh cho carousel
const images = ["images/hero.png", "images/hero_2.png", "images/hero_3.png"];
</script>

<style scoped>
.swiper-pagination-bullet-active {
    background-color: white;
}
</style>
