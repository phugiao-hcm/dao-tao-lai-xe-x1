<template>
    <section class="py-12 bg-white">
        <div class="container mx-auto px-4 space-y-12">
            <!-- Đội ngũ giáo viên -->
            <div>
                <h2 class="text-2xl md:text-3xl font-bold mb-6">
                    ĐỘI NGŨ GIÁO VIÊN TẠI Lái xe Phú Giáo
                </h2>
                <div
                    class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-5"
                >
                    <div
                        v-for="teacher in teachers"
                        :key="teacher.name"
                        class="rounded-xl overflow-hidden shadow-md hover:shadow-lg transition bg-white"
                    >
                        <img
                            :src="teacher.image"
                            alt="teacher"
                            class="w-full h-40 object-cover"
                        />
                        <div class="p-3">
                            <p class="font-semibold">{{ teacher.name }}</p>
                            <p class="text-sm text-red-500">
                                {{ teacher.role }}
                            </p>
                            <div
                                class="flex items-center justify-between text-gray-600 text-sm mt-2"
                            >
                                <span>👤 {{ teacher.experience }}</span>
                                <span>⭐ {{ teacher.rating }}</span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>

            <!-- Video học online -->
            <div>
                <h2 class="text-2xl md:text-3xl font-bold mb-6">
                    VIDEO HỌC ONLINE TẠI lái xe Phú Giáo
                </h2>
                <div
                    class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-4 gap-5"
                >
                    <div
                        v-for="video in videos"
                        :key="video.title"
                        class="rounded-xl overflow-hidden shadow-md hover:shadow-lg transition bg-white"
                    >
                        <img
                            :src="video.image"
                            alt="video"
                            class="w-full h-40 object-cover"
                        />
                        <div class="p-3">
                            <p class="font-semibold">{{ video.title }}</p>
                            <p class="text-sm text-red-500">
                                {{ video.label }}
                            </p>
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
        image: "/images/gv_1.png",
    },
    {
        name: "Trần Ngọc Nguyên",
        role: "GV Thực Hành",
        experience: "10 năm kinh nghiệm",
        rating: 5,
        image: "/images/gv_2.png",
    },
    {
        name: "Ngô Thiên Lương",
        role: "GV Lý Thuyết",
        experience: "5 năm kinh nghiệm",
        rating: 5,
        image: "/images/gv_3.png",
    },
    {
        name: "Nguyễn Minh Dũng",
        role: "GV Thực Hành",
        experience: "5 năm kinh nghiệm",
        rating: 5,
        image: "/images/gv_4.png",
    },
];

const videos = [
    {
        title: "600 Câu Hỏi Lý Thuyết lái Xe",
        label: "Miễn phí",
        views: "129.899",
        lessons: 12,
        duration: "3h12p",
        image: "/images/vd_1.png",
    },
    {
        title: "120 Tình Huống Mô Phỏng",
        label: "Miễn phí",
        views: "129.899",
        lessons: 14,
        duration: "3h12p",
        image: "/images/vd_2.png",
    },
    {
        title: "11 Bài Thi Sa Hình",
        label: "Miễn phí",
        views: "129.899",
        lessons: 1,
        duration: "3h12p",
        image: "/images/vd_3.png",
    },
    {
        title: "Mẹo Lái Xe Thực tế",
        label: "Miễn phí",
        views: "129.899",
        lessons: 15,
        duration: "3h12p",
        image: "/images/vd_4.png",
    },
];
</script>
