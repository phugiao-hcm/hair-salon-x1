<template>
  <transition name="fade-scale">
    <div
      v-if="show"
      class="fixed inset-0 bg-black/60 flex items-center justify-center z-50"
    >
      <div class="bg-white p-6 rounded-lg max-w-sm w-full relative shadow-lg">
        <button
          @click="show = false"
          class="absolute top-2 right-2 text-gray-400 hover:text-gray-600 text-xl"
        >
          ✕
        </button>
        <h3 class="text-xl font-bold mb-2 text-gray-800">Bạn cần hỗ trợ?</h3>
        <p class="mb-4 text-gray-600">Chat tư vấn miễn phí hoặc gọi hotline.</p>

        <a
          href="https://zalo.me/..."
          target="_blank"
          class="flex items-center justify-center gap-2 w-full bg-blue-500 hover:bg-blue-600 text-white py-2 rounded mb-2 transition"
        >
          <img src="/images/1.png" alt="Zalo" class="w-5 h-5" />
          Chat Zalo
        </a>
        <a
          href="https://facebook.com/..."
          target="_blank"
          class="flex items-center justify-center gap-2 w-full border border-blue-500 text-blue-500 hover:bg-blue-50 py-2 rounded transition"
        >
          <svg
            xmlns="http://www.w3.org/2000/svg"
            class="w-5 h-5"
            viewBox="0 0 24 24"
            fill="currentColor"
          >
            <path
              d="M22 12a10 10 0 10-11.5 9.87v-7h-2v-3h2v-2c0-2 1.2-3.1 3-3.1.9 0 1.8.2 1.8.2v2h-1c-1 0-1.3.6-1.3 1.2v1.7h2.5l-.4 3h-2.1v7A10 10 0 0022 12z"
            />
          </svg>
          Fanpage
        </a>
        <a
          href="tel:0987654321"
          class="mt-3 block text-center text-sm text-gray-500 hover:underline"
        >
          Gọi hotline: 0987 654 321
        </a>
      </div>
    </div>
  </transition>
</template>

<script setup>
import { ref, onMounted } from "vue";

const show = ref(false);

// Hiển thị sau 3 giây
onMounted(() => {
  setTimeout(() => {
    show.value = true;
  }, 3000);

  // Tự đóng sau 30 giây nếu không tương tác
  setTimeout(() => {
    show.value = false;
  }, 30000);
});
</script>

<style scoped>
.fade-scale-enter-active,
.fade-scale-leave-active {
  transition: opacity 0.3s, transform 0.3s;
}
.fade-scale-enter-from,
.fade-scale-leave-to {
  opacity: 0;
  transform: scale(0.95);
}
</style>
