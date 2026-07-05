<template>
    <section id="skills" class="w-full py-20 bg-[#0B1221] scroll-mt-24">
        <div class="max-w-5xl mx-auto px-5">
            <h2 class="text-center text-white font-bold text-2xl tracking-widest mb-16 uppercase" data-aos="fade-up">
                SKILLS
            </h2>
            
            <div class="grid grid-cols-2 sm:grid-cols-3 md:grid-cols-4 gap-y-12 gap-x-8 justify-items-center">
                <div v-for="(skill, index) in skills" :key="index" class="flex flex-col items-center group" data-aos="zoom-in" :data-aos-delay="index * 100">
                    <div class="w-16 h-16 md:w-20 md:h-20 flex items-center justify-center mb-4 transition-transform duration-300 group-hover:scale-110">
                        <i :class="[skill.icon, 'text-6xl md:text-7xl drop-shadow-md']"></i>
                    </div>
                    <span class="text-gray-300 font-medium text-sm md:text-base tracking-wide">{{ skill.name }}</span>
                </div>
            </div>
        </div>
    </section>
</template>

<script setup>
import { ref } from 'vue';

const skills = ref([
    { name: 'HTML5', icon: 'devicon-html5-plain colored' },
    { name: 'CSS3', icon: 'devicon-css3-plain colored' },
    { name: 'JavaScript', icon: 'devicon-javascript-plain colored' },
    { name: 'React.JS', icon: 'devicon-react-original colored' },
    { name: 'Tailwind CSS', icon: 'devicon-tailwindcss-plain colored' },
    { name: 'Git/Github', icon: 'devicon-git-plain colored' },
    { name: 'REST API', icon: 'devicon-postman-plain colored' }
]);
</script>