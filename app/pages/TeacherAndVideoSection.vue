<template>
  <section class="py-12 bg-white">
    <div class="container mx-auto px-4 space-y-12">
      <!-- Đội ngũ giáo viên -->
      <div>
        <h2 class="text-2xl md:text-3xl font-bold mb-6">
          ĐỘI NGŨ GIÁO VIÊN TẠI ĐẠT GIA
        </h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-5">
          <div
            v-for="teacher in teachers"
            :key="teacher.name"
            class="rounded-xl overflow-hidden border shadow-sm hover:shadow-md transition bg-white"
          >
            <img
              :src="teacher.image"
              alt="teacher"
              class="w-full h-40 object-cover"
            />
            <div class="p-3">
              <p class="font-semibold">{{ teacher.name }}</p>
              <p class="text-sm text-red-500">{{ teacher.role }}</p>
              <div
                class="flex items-center justify-between text-gray-600 text-sm mt-2"
              >
                <span>👤 {{ teacher.experience }}</span>
                <span>⭐ {{ teacher.rating }}</span>
              </div>
            </div>
          </div>
        </div>
        <div class="text-center mt-6">
          <button
            class="border border-blue-800 text-blue-800 px-4 py-2 rounded-md hover:bg-blue-50 transition"
          >
            XEM THÊM ĐỘI NGŨ
          </button>
        </div>
      </div>

      <!-- Video học online -->
      <div>
        <h2 class="text-2xl md:text-3xl font-bold mb-6">
          VIDEO HỌC ONLINE TẠI ĐẠT GIA
        </h2>
        <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-5">
          <div
            v-for="video in videos"
            :key="video.title"
            class="rounded-xl overflow-hidden border shadow-sm hover:shadow-md transition bg-white"
          >
            <img
              :src="video.image"
              alt="video"
              class="w-full h-40 object-cover"
            />
            <div class="p-3">
              <p class="font-semibold">{{ video.title }}</p>
              <p class="text-sm text-red-500">{{ video.label }}</p>
              <div
                class="flex items-center justify-between text-gray-600 text-sm mt-2 flex-wrap gap-2"
              >
                <span>👥 {{ video.views }}</span>
                <span>▶️ {{ video.lessons }}</span>
                <span>⏱️ {{ video.duration }}</span>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
const teachers = [
  {
    name: "Đồng Phát Đạt",
    role: "GV Lý thuyết",
    experience: "5 năm kinh nghiệm",
    rating: 5,
    image: "/teachers/teacher1.jpg",
  },
  {
    name: "Trần Ngọc Nguyên",
    role: "GV Thực Hành",
    experience: "10 năm kinh nghiệm",
    rating: 5,
    image: "/teachers/teacher2.jpg",
  },
  {
    name: "Ngô Thiên Lương",
    role: "GV Lý Thuyết",
    experience: "5 năm kinh nghiệm",
    rating: 5,
    image: "/teachers/teacher3.jpg",
  },
  {
    name: "Nguyễn Minh Dũng",
    role: "GV Thực Hành",
    experience: "5 năm kinh nghiệm",
    rating: 5,
    image: "/teachers/teacher4.jpg",
  },
];

const videos = [
  {
    title: "600 Câu Hỏi Lý Thuyết lái Xe",
    label: "Miễn phí",
    views: "129.899",
    lessons: 12,
    duration: "3h12p",
    image: "/videos/video1.jpg",
  },
  {
    title: "120 Tình Huống Mô Phỏng",
    label: "Miễn phí",
    views: "129.899",
    lessons: 14,
    duration: "3h12p",
    image: "/videos/video2.jpg",
  },
  {
    title: "11 Bài Thi Sa Hình",
    label: "Miễn phí",
    views: "129.899",
    lessons: 1,
    duration: "3h12p",
    image: "/videos/video3.jpg",
  },
  {
    title: "Mẹo Lái Xe Thực tế",
    label: "Miễn phí",
    views: "129.899",
    lessons: 15,
    duration: "3h12p",
    image: "/videos/video4.jpg",
  },
];
</script>
