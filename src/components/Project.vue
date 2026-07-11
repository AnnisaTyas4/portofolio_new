<template>
    <section id="project" class="relative w-full overflow-x-hidden py-14 sm:py-16 md:py-20 scroll-mt-24">
        <div class="w-full px-5 sm:px-8 md:px-12 lg:px-16 max-w-6xl mx-auto relative z-10">
            
            <div class="text-center mb-10 sm:mb-12 md:mb-16" data-aos="fade-up">
                <h2 class="text-white font-bold text-2xl sm:text-3xl md:text-4xl tracking-wide mb-6 sm:mb-8">PORTFOLIO</h2>
                
                <ul class="flex flex-wrap justify-center gap-4 sm:gap-6 md:gap-12 text-xs sm:text-sm md:text-base font-medium text-gray-400">
                    <li 
                        @click="activeTab = 'all'"
                        :class="activeTab === 'all' ? 'text-[#38bdf8]' : 'hover:text-white transition-colors'"
                        class="cursor-pointer">
                        All Project
                    </li>
                    <li 
                        @click="activeTab = 'website'"
                        :class="activeTab === 'website' ? 'text-[#38bdf8]' : 'hover:text-white transition-colors'"
                        class="cursor-pointer">
                        Website
                    </li>
                    <li 
                        @click="activeTab = 'mobile'"
                        :class="activeTab === 'mobile' ? 'text-[#38bdf8]' : 'hover:text-white transition-colors'"
                        class="cursor-pointer">
                        Mobile App 
                    </li>
                </ul>
            </div>

            <div v-if="activeTab === 'website' || activeTab === 'all'" class="grid lg:grid-cols-2 gap-10 lg:gap-16 items-center">
                
                <div class="flex flex-col order-2 lg:order-1 min-w-0" data-aos="fade-right">
                    <h3 class="text-[#38bdf8] text-sm sm:text-base md:text-lg font-semibold mb-2 tracking-wider uppercase">
                        PROJECT 1
                    </h3>
                    
                    <h2 class="text-white font-bold text-xl sm:text-2xl md:text-3xl lg:text-4xl leading-snug mb-4 break-words">
                        Maggo - Platform Pengelolaan Sampah Organik
                    </h2>
                    
                    <p class="text-gray-400 text-sm md:text-base leading-relaxed mb-8">
                        Maggo merupakan platform berbasis web yang menghubungkan masyarakat dengan peternak maggot untuk mendukung pengelolaan sampah organik yang lebih efektif. Pada proyek ini saya mengembangkan halaman Tentang Kami pada platform Maggo dengan mengimplementasikan desain dari Figma ke dalam aplikasi web menggunakan React.js. Fokus utama pada pembuatan tampilan responsif, penggunaan komponen yang reusable, dan memastikan pengalaman pengguna yang konsisten di berbagai ukuran layar.
                    </p>
                    
                </div>

                <div class="relative order-1 lg:order-2 flex justify-center lg:justify-end" data-aos="fade-left">
                    <div class="relative w-full max-w-[min(82vw,300px)] sm:max-w-[320px] lg:max-w-[350px]">
                        <div class="absolute inset-0 border-[5px] sm:border-[6px] border-[#38bdf8] -translate-x-3 translate-y-3 sm:-translate-x-4 sm:translate-y-4 md:-translate-x-6 md:translate-y-6 rounded-xl z-0"></div>
                        
                        <img 
                            src="../../src/assets/Maggo.jpeg" 
                            alt="Dating Mobile App Design" 
                            loading="lazy" 
                            class="relative z-10 w-full h-auto object-cover rounded-xl shadow-2xl bg-[#0B1221]"
                        >
                    </div>
                </div>

            </div>

            <div v-if="activeTab === 'mobile' || activeTab === 'all'" :class="['grid lg:grid-cols-2 gap-10 lg:gap-16 items-center', activeTab === 'all' ? 'mt-14 sm:mt-20 lg:mt-28' : '']">
                
                <div class="relative order-1 lg:order-1 flex justify-center lg:justify-start" data-aos="fade-right">
                    <div class="relative w-full max-w-[min(86vw,400px)] lg:max-w-[450px]">
                        <div class="absolute inset-0 border-[5px] sm:border-[6px] border-[#38bdf8] -translate-x-3 translate-y-3 sm:-translate-x-4 sm:translate-y-4 md:-translate-x-6 md:translate-y-6 rounded-xl z-0"></div>
                        
                        <img 
                            src="../../src/assets/Sitiga.png" 
                            alt="E Commerce Mobile App Design" 
                            loading="lazy" 
                            class="relative z-10 w-full h-auto object-cover rounded-xl shadow-2xl bg-[#0B1221]"
                        >
                    </div>
                </div>

                <div class="flex flex-col order-2 lg:order-2 min-w-0" data-aos="fade-left">
                    <h3 class="text-[#38bdf8] text-sm sm:text-base md:text-lg font-semibold mb-2 tracking-wider uppercase">
                        PROJECT 2
                    </h3>
                    
                    <h2 class="text-white font-bold text-xl sm:text-2xl md:text-3xl lg:text-4xl leading-snug mb-4 break-words">
                        SiTiga - Aplikasi Sistem Informasi Statistik Kota Salatiga
                    </h2>
                    
                    <p class="text-gray-400 text-sm md:text-base leading-relaxed mb-8">
                        SiTiga adalah aplikasi mobile yang dikembangkan untuk BPS Kota Salatiga guna mempermudah masyarakat dalam mengakses data statistik daerah. Aplikasi ini menampilkan data statistik secara real-time, publikasi berita resmi, serta mendukung akses data secara lebih cepat melalui mekanisme caching.Bertanggung jawab dalam pengembangan fitur tabel data yang menampilkan informasi statistik dari API BPS Kota Salatiga. Implementasi mencakup pengambilan data dari API, pengolahan data, serta penyajian informasi dalam bentuk tabel yang terstruktur dan mudah dibaca oleh pengguna.
                    </p>
                    
                </div>

            </div>

        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';
import { ArrowRightIcon } from '@heroicons/vue/16/solid';

const activeTab = ref('all');
</script>