<template>
    <div>
        <HeroSection id="hero" />
        <CoursesSection id="courses" />
        <TestimonialsSection />
        <TeacherAndVideoSection id="team" />
    </div>
</template>

<script setup>
import HeroSection from "./home/HeroSection.vue";
import CoursesSection from "./home/CoursesSection.vue";
import TestimonialsSection from "./home/TestimonialsSection.vue";
import TeacherAndVideoSection from "./home/TeacherAndVideoSection.vue";
</script>
