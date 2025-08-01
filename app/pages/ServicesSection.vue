<template>
  <section id="services" class="py-16 bg-gray-50 text-center">
    <h2 class="text-3xl font-bold mb-8">Dịch vụ của chúng tôi</h2>
    <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6 px-4">
      <div
        v-for="sv in services"
        :key="sv.title"
        class="bg-white p-6 rounded-lg shadow hover:shadow-lg transition"
      >
        <img :src="sv.icon" class="w-16 h-16 mx-auto mb-4" />
        <h3 class="font-semibold text-xl">{{ sv.title }}</h3>
        <p class="mt-2 text-gray-600">{{ sv.desc }}</p>
      </div>
    </div>
  </section>
</template>
<script setup>
const services = [
  {
    title: "Cắt tóc chuyên nghiệp",
    desc: "Tư vấn phù hợp với cá tính bạn.",
    icon: "/images/icon-cut.png",
  },
  {
    title: "Nhuộm & highlight",
    desc: "Màu bền đẹp, lên tone chuẩn.",
    icon: "/images/icon-color.png",
  },
  {
    title: "Uốn & duỗi",
    desc: "Tóc vào nếp tự nhiên, mượt mà.",
    icon: "/images/icon-perm.png",
  },
  {
    title: "Chăm sóc & phục hồi",
    desc: "Phục hồi tóc hư tổn chuyên sâu.",
    icon: "/images/icon-care.png",
  },
];
</script>
