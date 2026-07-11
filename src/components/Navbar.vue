<template>
    <div class="text-white font-sans fixed w-full top-0 z-50 bg-[#0B1221]/90 backdrop-blur-md">
        <header class="flex justify-between items-center px-4 sm:px-6 lg:px-8 py-4 sm:py-5 bg-opacity-50 relative z-20">
            <div class="text-2xl sm:text-3xl font-bold bg-linear-to-r from-blue-400 to-cyan-400 bg-clip-text text-transparent">
                Tyas 
            </div>
            
            <div class="md:hidden z-30">
                <button type="button"
                class="block focus:outline-none p-2 rounded-lg bg-blue-800/50 hover:bg-blue-700/50 transition-all duration-300"
                @click="isMenuOpen = !isMenuOpen"
                >
                <div class="relative w-6 h-6">
                    <span :class="[
                        'absolute left-0 w-6 h-0.5 bg-blue-200 transition-all duration-300',
                        isMenuOpen ? 'rotate-45 top-3' : 'top-1'
                    ]"></span>
                    <span :class="[
                        'absolute left-0 w-6 h-0.5 bg-blue-200 transition-all duration-300',
                        isMenuOpen ? 'opacity-0' : 'top-3 opacity-100'
                    ]"></span>
                    <span :class="[
                        'absolute left-0 w-6 h-0.5 bg-blue-200 transition-all duration-300',
                        isMenuOpen ? '-rotate-45 top-3' : 'top-5'
                    ]"></span>
                </div>
                </button>
            </div>
            
            <nav
            :class=" [
                'absolute top-full left-0 w-full max-h-[calc(100svh-72px)] overflow-y-auto bg-[#0B1221]/95 border-b border-gray-800 shadow-xl md:max-h-none md:overflow-visible md:shadow-none md:border-none md:bg-transparent md:static md:w-auto transition-all duration-300',
                isMenuOpen ? 'block' : 'hidden md:block'
            ]">
                <ul class="flex flex-col items-center px-6 py-5 space-y-5 md:flex-row md:items-center md:space-x-8 lg:space-x-10 md:space-y-0 md:p-0 md:justify-center md:ml-auto">
                    <li v-for="item in Menu" :key="item.name" class="group relative w-max">
                        <a :href="item.href"
                        class="relative block text-blue-100 hover:text-blue-400 transition-all duration-300 text-base md:text-sm lg:text-base font-medium tracking-wide group"
                        @click="ScrollToSection(item.href)">    
                        {{ item.name }}
                            <span class="absolute bottom-0 left-0 w-0 h-0.5 bg-blue-400 transition-all duration-300 group-hover:w-full"></span>
                        </a>
                    </li>
                </ul>
                
            </nav>
        </header>
    </div>
</template>

<script setup>
import { ref } from 'vue';

const Menu = ref([
    { name: 'HOME', href: '#home' },
    { name: 'ABOUT ME', href: '#about' },
    { name: 'SKILLS', href: '#skills' },
    { name: 'PROJECT', href: '#project' }
]);

const isMenuOpen = ref(false);

const ScrollToSection = (href) => {
    isMenuOpen.value = false;
    const Section = document.querySelector(href);
    if(Section) {
        Section.scrollIntoView({ behavior: 'smooth' });
    }
}
</script>