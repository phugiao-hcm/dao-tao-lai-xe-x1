<template>
  <section id="team" class="py-16 px-4">
    <div class="max-w-5xl mx-auto text-center mb-8">
      <h2 class="text-3xl font-semibold">Hành trình học viên</h2>
    </div>
    <div class="grid grid-cols-1 md:grid-cols-2 gap-6 max-w-5xl mx-auto">
      <div
        v-for="t in testimonials"
        :key="t.id"
        class="bg-white p-6 rounded-lg shadow"
      >
        <p class="text-gray-700 mb-4">“{{ t.review }}”</p>
        <h4 class="font-semibold">{{ t.name }}</h4>
        <p class="text-sm text-gray-500">
          Thời gian hoàn thành: {{ t.duration }}
        </p>
      </div>
    </div>
  </section>
</template>

<script setup>
const testimonials = [
  {
    id: 1,
    name: "Nguyễn Duy Minh",
    review: "Đã cấp bằng: 129.899 học viên",
    duration: "3h12p",
  },
  {
    id: 2,
    name: "Đinh Thế Bảo",
    review: "Đã cấp bằng: 129.899 học viên",
    duration: "3h12p",
  },
];
</script>
