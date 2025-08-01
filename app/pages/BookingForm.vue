<template>
  <section id="booking" class="py-16 bg-gray-100 text-center px-4">
    <h2 class="text-3xl font-bold mb-6">Đặt lịch ngay</h2>
    <form class="max-w-md mx-auto space-y-4">
      <input
        type="text"
        placeholder="Họ và tên"
        class="w-full border rounded px-3 py-2"
      />
      <input
        type="text"
        placeholder="Số điện thoại"
        class="w-full border rounded px-3 py-2"
      />
      <select class="w-full border rounded px-3 py-2">
        <option>Dịch vụ bạn muốn chọn</option>
        <option>Cắt tóc</option>
        <option>Nhuộm tóc</option>
        <option>Chăm sóc tóc</option>
      </select>
      <button
        type="submit"
        class="w-full bg-pink-500 text-white py-2 rounded hover:bg-pink-600"
      >
        Gửi yêu cầu
      </button>
    </form>
  </section>
</template>
