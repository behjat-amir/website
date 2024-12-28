<script setup>
import { Head } from '@inertiajs/vue3';
import { ref, onMounted } from 'vue';
import LottieAnimation from '@/Components/LottieAnimation.vue';

const skills = {
    frontend: [
        { name: 'Vue.js', level: 90, icon: '⚡️' },
        { name: 'Nuxt.js', level: 20, icon: '🚀' },
        { name: 'Vuetify', level: 90, icon: '🎨' },
    ],
    backend: [
        { name: 'Laravel', level: 90, icon: '🐘' },
        { name: 'Spring Boot', level: 50, icon: '💚' },
    ],
    database: [
        { name: 'Oracle', level: 85, icon: '🍃' },
        { name: 'Mysql', level: 100, icon: '📕' },
    ],
    devops: [
        { name: 'Docker', level: 60, icon: '🐳' },
        { name: 'Linux', level: 95, icon: '🐧' },
        { name: 'Nginx', level: 85, icon: '🌐' },
        { name: 'Git', level: 90, icon: '📚' },
    ],
    mobile: [
        { name: 'Flutter', level: 40, icon: '📱' },
    ],
    ai: [
        { name: 'TensorFlow', level: 30, icon: '🧠' },
        { name: 'PyTorch', level: 35, icon: '🔥' },
    ],
    tools: [
        { name: 'Figma', level: 90, icon: '🎨' },
        { name: 'Postman', level: 100, icon: '📮' },
    ]
};

const personalInfo = {
    name: 'امیرحسین نوروزی بهجت',
    title: 'Full Stack Developer',
    email: 'amirw.noroozi@gmail.com',
    location: 'رفسنجان، ایران',
    about: 'توسعه‌دهنده Full Stack با تخصص در Flutter ، PHP (Laravel)، Java و تکنولوژی‌های مدرن وب. در حال حاضر مشغول کار بر روی پروژه‌  شخصی ( بگذر ) هستم.',
    github: 'https://github.com/behjat-amir',
    telegram: 'noroozi_amir',
    instagram: 'amir.norowzi',
    phone: '+98 935 072 6665',
    github: 'https://github.com/behjat-amir',
    achievements: ['Arctic Code Vault Contributor'],
    projects: [
        {
            name: 'BlueStone',
            description: 'کتابخانه PHP برای سات آسان ربات‌های تلگرام',
            stars: 35
        },
        {
            name: 'xMusic',
            description: 'API دانلود موسیقی فارسی',
            stars: 100
        },
        {
            name: 'BDR',
            description: 'کتابخانه رمزنگاری و هش‌کننده رشته‌های PHP',
            stars: 10
        },
        {
            name: 'Begzar',
            description: 'نرم افزار تحریم شکن کراس پلتفرم',
            stars: 340
        }
    ]
};

const activeSection = ref('frontend');
const isLoaded = ref(false);

onMounted(() => {
    isLoaded.value = true;
});
</script>

<template>

    <Head title="خانه" />

    <div class="min-h-screen bg-[#0f172a] text-white">
        <!-- Hero Section -->
        <div class="relative overflow-hidden">
            <!-- Animated Background -->
            <div class="absolute inset-0">
                <div class="absolute inset-0 bg-gradient-to-b from-[#090c11] to-[#0f172a]"></div>
                <div
                    class="absolute inset-0 opacity-30 bg-[radial-gradient(#ffffff33_1px,transparent_1px)] [background-size:16px_16px]">
                </div>

            </div>

            <div class="relative max-w-7xl mx-auto px-4 pt-20 pb-32">
                <div class="text-center">
                    <!-- Profile Section -->
                    <div class="mb-12">
                        <div class="relative inline-block">
                            <div
                                class="absolute inset-0 bg-gradient-to-r from-[#3b82f6] to-[#8b5cf6] blur-3xl opacity-20">
                            </div>
                            <img src="/assets/img/profile.jpg" alt="Profile"
                                class="relative w-44 h-44 rounded-full border-4 border-white/10 shadow-2xl">
                        </div>
                    </div>

                    <!-- Name & Title -->
                    <h1
                        class="text-5xl font-yekanbakhextrabold mb-4 bg-gradient-to-r from-[#3b82f6] to-[#8b5cf6] bg-clip-text text-transparent">
                        {{ personalInfo.name }}
                    </h1>
                    <div
                        class="inline-flex items-center gap-2 px-6 py-2 rounded-full bg-white/5 backdrop-blur-sm border border-white/10 mb-8">
                        <span class="text-xl text-white/80">{{ personalInfo.title }}</span>
                    </div>

                    <!-- About -->
                    <p class="max-w-2xl mx-auto font-yekanbakh text-lg text-white/60 leading-relaxed mb-12" dir="rtl">
                        {{ personalInfo.about }}
                    </p>

                    <!-- Contact Info Section -->
                    <div class="relative py-16">
                        <!-- Background Overlay -->
                        <div class="absolute inset-0 bg-gradient-to-b from-transparent via-blue-500/5 to-transparent">
                        </div>

                        <!-- Content -->
                        <div class="relative max-w-5xl mx-auto">
                            <!-- Section Title -->
                            <div class="flex justify-center items-center mb-12 gap-3">
                                <h2 class="text-3xl font-yekanbakhextrabold text-center">

                                    <span
                                        class="bg-gradient-to-r from-[#3b82f6] to-[#8b5cf6] bg-clip-text text-transparent">
                                        راه‌های ارتباطی
                                    </span>
                                </h2>
                            </div>


                            <!-- Contact Grid -->
                            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6 px-4">
                                <!-- Email -->
                                <a :href="`mailto:${personalInfo.email}`" class="contact-card group">
                                    <div class="contact-icon-wrapper bg-blue-500/10">
                                        <svg class="w-7 h-7 text-blue-500" fill="none" stroke="currentColor"
                                            viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                                                d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                                        </svg>
                                    </div>
                                    <div class="flex flex-col">
                                        <span class="contact-label">ایمیل</span>
                                        <span class="contact-value">{{ personalInfo.email }}</span>
                                    </div>
                                </a>

                                <!-- Telegram -->
                                <a :href="`https://t.me/${personalInfo.telegram}`" class="contact-card group">
                                    <div class="contact-icon-wrapper bg-[#229ED9]/10">
                                        <svg class="w-7 h-7 text-[#229ED9]" viewBox="0 0 24 24" fill="currentColor">
                                            <path
                                                d="M12 2C6.48 2 2 6.48 2 12s4.48 10 10 10 10-4.48 10-10S17.52 2 12 2zm4.64 6.8c-.15 1.58-.8 5.42-1.13 7.19-.14.75-.42 1-.68 1.03-.58.05-1.02-.38-1.58-.75-.88-.58-1.38-.94-2.23-1.5-.99-.65-.35-1.01.22-1.59.15-.15 2.71-2.48 2.76-2.69a.2.2 0 00-.05-.18c-.06-.05-.14-.03-.21-.02-.09.02-1.49.95-4.22 2.79-.4.27-.76.41-1.08.4-.36-.01-1.04-.2-1.55-.37-.63-.2-1.12-.31-1.08-.66.02-.18.27-.36.74-.55 2.92-1.27 4.86-2.11 5.83-2.51 2.78-1.16 3.35-1.36 3.73-1.36.08 0 .27.02.39.12.1.08.13.19.14.27-.01.06.01.24 0 .24z" />
                                        </svg>
                                    </div>
                                    <div class="flex flex-col">
                                        <span class="contact-label">تلگرام</span>
                                        <span class="contact-value">{{ personalInfo.telegram }}</span>
                                    </div>
                                </a>

                                <!-- Instagram -->
                                <a :href="`https://instagram.com/${personalInfo.instagram}`" class="contact-card group">
                                    <div
                                        class="contact-icon-wrapper bg-gradient-to-br from-purple-500/10 to-pink-500/10">
                                        <svg class="w-7 h-7 text-pink-500" viewBox="0 0 24 24" fill="currentColor">
                                            <path
                                                d="M12 2c2.717 0 3.056.01 4.122.06 1.065.05 1.79.217 2.428.465.66.254 1.216.598 1.772 1.153a4.908 4.908 0 0 1 1.153 1.772c.247.637.415 1.363.465 2.428.047 1.066.06 1.405.06 4.122 0 2.717-.01 3.056-.06 4.122-.05 1.065-.218 1.79-.465 2.428a4.883 4.883 0 0 1-1.153 1.772 4.915 4.915 0 0 1-1.772 1.153c-.637.247-1.363.415-2.428.465-1.066.047-1.405.06-4.122.06-2.717 0-3.056-.01-4.122-.06-1.065-.05-1.79-.218-2.428-.465a4.89 4.89 0 0 1-1.772-1.153 4.904 4.904 0 0 1-1.153-1.772c-.248-.637-.415-1.363-.465-2.428C2.013 15.056 2 14.717 2 12c0-2.717.01-3.056.06-4.122.05-1.066.217-1.79.465-2.428a4.88 4.88 0 0 1 1.153-1.772A4.897 4.897 0 0 1 5.45 2.525c.638-.248 1.362-.415 2.428-.465C8.944 2.013 9.283 2 12 2zm0 5a5 5 0 1 0 0 10 5 5 0 0 0 0-10zm6.5-.25a1.25 1.25 0 0 0-2.5 0 1.25 1.25 0 0 0 2.5 0zM12 9a3 3 0 1 1 0 6 3 3 0 0 1 0-6z" />
                                        </svg>
                                    </div>
                                    <div class="flex flex-col">
                                        <span class="contact-label">اینستاگرام</span>
                                        <span class="contact-value">{{ personalInfo.instagram }}</span>
                                    </div>
                                </a>

                                <!-- GitHub -->
                                <a :href="personalInfo.github" class="contact-card group">
                                    <div class="contact-icon-wrapper bg-gray-800/10">
                                        <svg class="w-7 h-7" viewBox="0 0 24 24" fill="currentColor">
                                            <path
                                                d="M12 2C6.477 2 2 6.477 2 12c0 4.42 2.87 8.17 6.84 9.5.5.08.66-.23.66-.5v-1.69c-2.77.6-3.36-1.34-3.36-1.34-.46-1.16-1.11-1.47-1.11-1.47-.91-.62.07-.6.07-.6 1 .07 1.53 1.03 1.53 1.03.87 1.52 2.34 1.07 2.91.83.09-.65.35-1.09.63-1.34-2.22-.25-4.55-1.11-4.55-4.92 0-1.11.38-2 1.03-2.71-.1-.25-.45-1.29.1-2.64 0 0 .84-.27 2.75 1.02.79-.22 1.65-.33 2.5-.33.85 0 1.71.11 2.5.33 1.91-1.29 2.75-1.02 2.75-1.02.55 1.35.2 2.39.1 2.64.65.71 1.03 1.6 1.03 2.71 0 3.82-2.34 4.66-4.57 4.91.36.31.69.92.69 1.85V21c0 .27.16.59.67.5C19.14 20.16 22 16.42 22 12A10 10 0 0012 2z" />
                                        </svg>
                                    </div>
                                    <div class="flex flex-col">
                                        <span class="contact-label">گیت هاب</span>
                                        <span class="contact-value">github.com/behjat-amir</span>
                                    </div>
                                </a>

                                <!-- Phone -->
                                <a :href="`tel:${personalInfo.phone}`" class="contact-card group">
                                    <div class="contact-icon-wrapper bg-green-500/10">
                                        <svg class="w-7 h-7 text-green-500" fill="none" stroke="currentColor"
                                            viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                                                d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                                        </svg>
                                    </div>
                                    <div class="flex flex-col">
                                        <span class="contact-label">شماره تماس</span>
                                        <span class="contact-value">{{ personalInfo.phone }}</span>
                                    </div>
                                </a>

                                <!-- Location -->
                                <div class="contact-card">
                                    <div class="contact-icon-wrapper bg-blue-500/10">
                                        <svg class="w-7 h-7 text-blue-500" fill="none" stroke="currentColor"
                                            viewBox="0 0 24 24">
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                                                d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5"
                                                d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                                        </svg>
                                    </div>
                                    <div class="flex flex-col">
                                        <span class="contact-label">موقعیت</span>
                                        <span class="contact-value font-yekanbakh">{{ personalInfo.location }}</span>
                                    </div>
                                </div>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Skills Section -->
        <div class="relative">
            <div class="max-w-7xl mx-auto px-4 py-24">
                <!-- Section Title -->
                <div class="flex justify-center items-center mb-12 gap-3">
                                <LottieAnimation path="/assets/animations/check.json" width="60px" height="60px"
                                :speed="1" />
                                <h2 class="text-3xl font-yekanbakhextrabold text-center">

                                    <span
                                        class="bg-gradient-to-r from-[#3b82f6] to-[#8b5cf6] bg-clip-text text-transparent">
                                       مهارت های من
                                    </span>
                                </h2>
                            </div>

                <!-- All Skills Grid -->
                <div class="grid grid-cols-1 md:grid-cols-3 lg:grid-cols-4 gap-6">
                    <template v-for="(skillGroup, category) in skills" :key="category">
                        <div v-for="skill in skillGroup" :key="skill.name"
                            class="group relative bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:bg-white/10 transition-all duration-300">
                            <div class="flex items-center gap-4 mb-4">
                                <span class="text-2xl">{{ skill.icon }}</span>
                                <h3 class="text-lg font-medium">{{ skill.name }}</h3>
                            </div>

                            <div class="relative h-2 bg-white/10 rounded-full overflow-hidden">
                                <div class="absolute top-0 left-0 h-full w-0 bg-gradient-to-r from-[#3b82f6] to-[#8b5cf6] rounded-full transition-all duration-1000 group-hover:duration-700"
                                    :style="{ width: `${skill.level}%` }">
                                    <div class="absolute inset-0 bg-white/20 animate-[shimmer_2s_infinite]"></div>
                                </div>
                            </div>

                            <div class="absolute top-4 right-4 text-sm font-medium text-white/60">
                                {{ skill.level }}%
                            </div>

                            <div class="absolute bottom-1 right-4 text-xs font-medium text-white/40 uppercase">
                                {{ category }}
                            </div>
                        </div>
                    </template>
                </div>
            </div>
        </div>

        <!-- Projects Section -->
        <div class="relative" dir="rtl">
            <div class="max-w-7xl mx-auto px-4 py-24">
                <div class="flex justify-center items-center mb-12 gap-3">

                                <h2 class="text-3xl font-yekanbakhextrabold text-center">

                                    <span
                                        class="bg-gradient-to-r from-[#3b82f6] to-[#8b5cf6] bg-clip-text text-transparent">
                                       پروژه ها
                                    </span>
                                </h2>
                                <LottieAnimation path="/assets/animations/github.json" width="60px" height="60px"
                                :speed="2" />
                            </div>

                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
                    <div v-for="project in personalInfo.projects" :key="project.name"
                        class="group relative bg-white/5 backdrop-blur-sm rounded-xl p-6 border border-white/10 hover:bg-white/10 transition-all duration-300">
                        <h3 class="text-xl font-medium mb-2">{{ project.name }}</h3>
                        <p class="text-white/60 mb-4 font-yekanbakh">{{ project.description }}</p>
                        <div class="flex items-center gap-2">
                            <span class="text-yellow-500">⭐</span>
                            <span class="text-white/60">{{ project.stars }}</span>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <!-- Portfolio Section -->
        <div class="relative" dir="rtl">
            <div class="max-w-7xl mx-auto px-4 py-24">
                <!-- Section Title -->
                <div class="flex justify-center items-center mb-12 gap-3">

                                <h2 class="text-3xl font-yekanbakhextrabold text-center">

                                    <span
                                        class="bg-gradient-to-r from-[#3b82f6] to-[#8b5cf6] bg-clip-text text-transparent">
                                        نمونه کار ها
                                    </span>
                                </h2>
                                <LottieAnimation path="/assets/animations/flame.json" width="40px" height="40px"
                                :speed="1" />
                            </div>

                <!-- Portfolio Grid -->
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 font-yekanbakh">
                    <!-- Digialat -->
                    <a href="http://digialat.com/" target="_blank" 
                        class="group relative overflow-hidden rounded-2xl bg-white/5 border border-white/10 hover:bg-white/10 transition-all duration-300 hover:scale-[1.02]"
                    >
                        <div class="aspect-video w-full bg-gradient-to-br from-blue-500/20 to-purple-500/20">
                            <img 
                                src="/assets/img/digialat.png" 
                                alt="Digialat" 
                                class="w-full h-full object-cover opacity-80 group-hover:opacity-100 transition-opacity"
                            >
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-medium mb-2 font-yekanbakhextrabold">دیجی آلات</h3>
                            <p class="text-white/60 font-yekanbakh text-sm">
                                فروشگاه آنلاین قطعات و تجهیزات صنعتی
                            </p>
                        </div>
                        <div class="absolute top-4 left-4">
                            <span class="px-3 py-1 rounded-full bg-white/10 backdrop-blur-sm text-xs">
                                Laravel + Vue.js
                            </span>
                        </div>
                    </a>

                    <!-- Ex-bitbank -->
                    <a href="http://ex-bitbank.info/" target="_blank"
                        class="group relative overflow-hidden rounded-2xl bg-white/5 border border-white/10 hover:bg-white/10 transition-all duration-300 hover:scale-[1.02]"
                    >
                        <div class="aspect-video w-full bg-gradient-to-br from-green-500/20 to-blue-500/20">
                            <img 
                                src="/assets/img/bitbank.png" 
                                alt="Ex-bitbank" 
                                class="w-full h-full object-cover opacity-80 group-hover:opacity-100 transition-opacity"
                            >
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-medium mb-2 font-yekanbakhextrabold">بیت بانک</h3>
                            <p class="text-white/60 font-yekanbakh text-sm">
                                پلتفرم خرید و فروش ارزهای دیجیتال
                            </p>
                        </div>
                        <div class="absolute top-4 left-4">
                            <span class="px-3 py-1 rounded-full bg-white/10 backdrop-blur-sm text-xs">
                                Node.js + React
                            </span>
                        </div>
                    </a>

                    <!-- Odinnet -->
                    <a href="http://odinnet.pro/" target="_blank"
                        class="group relative overflow-hidden rounded-2xl bg-white/5 border border-white/10 hover:bg-white/10 transition-all duration-300 hover:scale-[1.02]"
                    >
                        <div class="aspect-video w-full bg-gradient-to-br from-purple-500/20 to-pink-500/20">
                            <img 
                                src="/assets/img/odinnet.png" 
                                alt="Odinnet" 
                                class="w-full h-full object-cover opacity-80 group-hover:opacity-100 transition-opacity"
                            >
                        </div>
                        <div class="p-6">
                            <h3 class="text-xl font-medium mb-2 font-yekanbakhextrabold">اُدین نت</h3>
                            <p class="text-white/60 font-yekanbakh text-sm">
                                سرویس‌های شبکه و زیرساخت
                            </p>
                        </div>
                        <div class="absolute top-4 left-4">
                            <span class="px-3 py-1 rounded-full bg-white/10 backdrop-blur-sm text-xs">
                                PHP + Vue.js
                            </span>
                        </div>
                    </a>
                </div>
            </div>
        </div>
    </div>
</template>

<style scoped>
@keyframes shimmer {
    0% {
        transform: translateX(-100%);
    }

    100% {
        transform: translateX(100%);
    }
}

.contact-card {
    @apply flex items-center gap-4 p-4 rounded-2xl bg-white/5 hover:bg-white/10 border border-white/10 backdrop-blur-sm transition-all duration-300 hover:scale-[1.02] hover:shadow-lg hover:shadow-blue-500/10;
}

.contact-icon-wrapper {
    @apply p-3 rounded-xl transition-all duration-300 group-hover:scale-110;
}

.contact-label {
    @apply text-xs text-white/40 font-yekanbakh;
}

.contact-value {
    @apply text-sm text-white/90 transition-colors duration-300 group-hover:text-white;
}
</style>
