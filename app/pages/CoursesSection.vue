<template>
  <section class="py-12 bg-white">
    <div class="container mx-auto px-4 text-center">
      <h2 class="text-2xl md:text-3xl font-bold mb-10">KHÓA HỌC LÁI XE Ô TÔ</h2>

      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
        <div
          v-for="course in courses"
          :key="course.id"
          class="rounded-xl overflow-hidden border shadow hover:shadow-lg transition bg-white"
        >
          <!-- Hình ảnh + tiêu đề -->
          <div class="relative h-48">
            <img
              :src="course.image"
              alt="course"
              class="object-cover w-full h-full"
            />
            <div
              class="absolute inset-0 bg-black/40 flex flex-col items-center justify-center text-white text-xl font-bold"
            >
              <p>{{ course.title }}</p>
              <p class="text-sm font-normal">{{ course.subtitle }}</p>
            </div>
          </div>

          <!-- Nội dung chính -->
          <div class="text-left px-5 py-4">
            <p class="font-bold mb-3 uppercase">Đã bao gồm</p>
            <ul class="space-y-2 text-sm">
              <li
                v-for="(item, i) in course.features"
                :key="i"
                class="flex items-start gap-2"
              >
                <span class="text-green-600 mt-0.5">✅</span>
                <span>{{ item }}</span>
              </li>
            </ul>

            <p class="text-red-600 font-bold text-center mt-4 text-lg">
              HỖ TRỢ HỌC ĐẬU
            </p>
          </div>

          <!-- Giá -->
          <div class="bg-[#002f63] text-white text-center py-4">
            <p class="text-xl font-bold text-orange-400">{{ course.price }}</p>
            <p class="line-through text-sm text-red-400 mt-1">
              {{ course.oldPrice }}
            </p>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const courses = [
  {
    id: 1,
    title: "HỌC BẰNG B",
    subtitle: "Tự động",
    image: "/course-b-auto.jpg",
    price: "18.400.000 VND",
    oldPrice: "21.400.000 VND",
    features: [
      "Học phí trọn gói không phát sinh",
      "Trả góp 0% lãi suất",
      "Giáo viên tận tâm - trách nhiệm (5 năm kinh nghiệm)",
      "Học thứ 7, chủ nhật không phụ thu thêm",
      "Bằng do sở GTVT cấp kèm hồ sơ gốc",
    ],
  },
  {
    id: 2,
    title: "HỌC BẰNG B",
    subtitle: "Cơ khí",
    image: "/course-b-manual.jpg",
    price: "21.200.000 VND",
    oldPrice: "24.200.000 VND",
    features: [
      "Học phí trọn gói không phát sinh",
      "Trả góp 0% lãi suất",
      "Giáo viên tận tâm - trách nhiệm (5 năm kinh nghiệm)",
      "Học thứ 7, chủ nhật không phụ thu thêm",
      "Bằng do sở GTVT cấp kèm hồ sơ gốc",
    ],
  },
  {
    id: 3,
    title: "HỌC BẰNG C1",
    subtitle: "",
    image: "/course-c1.jpg",
    price: "22.965.000 VND",
    oldPrice: "26.965.000 VND",
    features: [
      "Học phí trọn gói không phát sinh",
      "Trả góp 0% lãi suất",
      "Giáo viên tận tâm - trách nhiệm (5 năm kinh nghiệm)",
      "Học thứ 7, chủ nhật không phụ thu thêm",
      "Bằng do sở GTVT cấp kèm hồ sơ gốc",
    ],
  },
];
</script>
