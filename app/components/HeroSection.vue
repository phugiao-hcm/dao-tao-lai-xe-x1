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
        <img :src="img" alt="hero image" class="object-cover w-full h-full" />
      </SwiperSlide>
    </Swiper>

    <div class="absolute inset-0 bg-black/40 flex items-center justify-center">
      <div class="text-white text-center space-y-2">
        <h1 class="text-xl sm:text-2xl md:text-4xl font-bold">
          Trung tâm đào tạo lái xe Đạt Gia
        </h1>
        <p class="text-sm sm:text-base">Học lái xe ô tô B1, B2, C tại TP.HCM</p>
      </div>
    </div>
  </section>
</template>

<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Autoplay, Pagination } from "swiper/modules";
import "swiper/css";
import "swiper/css/pagination";

const images = ["/hero1.jpg", "/hero2.jpg", "/hero3.jpg"];
</script>

<style scoped>
.swiper-pagination-bullet-active {
  background-color: white;
}
</style>
