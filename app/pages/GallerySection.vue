<template>
  <section class="py-12 bg-gray-50">
    <h2 class="text-3xl font-bold text-center mb-8">
      Khách hàng tại Salon Đông
    </h2>
    <div class="grid grid-cols-4 gap-4 px-4 max-w-5xl mx-auto">
      <div
        v-for="(img, idx) in images"
        :key="idx"
        class="overflow-hidden rounded-lg shadow-lg"
      >
        <img
          :src="img"
          alt="Khách hàng salon"
          class="w-full h-56 object-cover"
        />
      </div>
    </div>
  </section>
</template>

<script setup>
const images = [
  "/images/customer1.jpg",
  "/images/customer2.jpg",
  "/images/customer3.jpg",
  "/images/customer4.jpg",
];
</script>
