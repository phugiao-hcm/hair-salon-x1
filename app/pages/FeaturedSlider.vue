<template>
    <section id="portfolio" class="py-16 px-4 bg-white">
        <h2 class="text-3xl font-bold text-center mb-8">Mẫu tóc nổi bật</h2>
        <Swiper
            :modules="[Navigation]"
            :slides-per-view="1.2"
            :space-between="16"
            :breakpoints="{
                640: { slidesPerView: 2.2 },
                1024: { slidesPerView: 3.3 },
            }"
            navigation
            class="max-w-6xl mx-auto"
        >
            <SwiperSlide
                v-for="(img, i) in images"
                :key="i"
                class="rounded overflow-hidden"
            >
                <img :src="img" class="w-full h-60 object-cover" />
            </SwiperSlide>
        </Swiper>
    </section>
</template>
<script setup>
import { Swiper, SwiperSlide } from "swiper/vue";
import { Navigation } from "swiper/modules";
import "swiper/css";
import "swiper/css/navigation";
const images = [
    "images/feature_1.png",
    "images/feature_2.png",
    "images/feature_3.png",
    "images/feature_4.png",
];
</script>
