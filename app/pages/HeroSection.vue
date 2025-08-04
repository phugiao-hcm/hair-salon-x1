<template>
    <section id="home" class="relative h-[500px] overflow-hidden">
        <video
            autoplay
            muted
            loop
            playsinline
            class="absolute inset-0 w-full h-full object-cover"
        >
            <source src="/videos/hero_ads.mp4" type="video/mp4" />
        </video>
        <div class="absolute inset-0 bg-black/40"></div>
        <div
            class="relative z-10 flex flex-col items-center justify-center h-full text-white px-4 text-center"
        >
            <h1 class="text-4xl md:text-6xl font-bold">Salon Phú Giáo</h1>
            <p class="mt-3 text-lg md:text-2xl">
                Kiến tạo phong cách – chăm sóc tận tình
            </p>
            <NuxtLink
                to="#booking"
                class="mt-6 bg-pink-500 hover:bg-pink-600 py-3 px-6 rounded text-white font-medium"
            >
                Đặt lịch ngay
            </NuxtLink>
        </div>
    </section>
</template>
