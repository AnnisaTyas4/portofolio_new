<template>
    <section id="about" class="relative w-full overflow-x-hidden py-12 md:py-16 scroll-mt-24">
        <div class="w-full px-5 sm:px-8 md:px-12 lg:px-8 max-w-5xl lg:max-w-5xl mx-auto relative z-10">
            <div class="grid lg:grid-cols-2 gap-12 xl:gap-20 items-center">
                
                <div class="flex justify-center lg:justify-start" data-aos="fade-right">
                    <div class="relative w-full max-w-[320px] sm:max-w-[400px]">
                        <div class="absolute inset-0 border-[6px] border-[#38bdf8] translate-x-6 translate-y-6 md:translate-x-8 md:translate-y-8 rounded-lg z-0"></div>
                        
                        <img 
                            src="../../src/assets/about.jpeg" 
                            alt="About Me" 
                            loading="lazy" 
                            class="relative z-10 w-full h-auto object-cover rounded-lg shadow-xl"
                        >
                    </div>
                </div>
 
                <div class="flex flex-col mt-16 lg:mt-0 justify-center" data-aos="fade-left">
                    <h2 class="text-white font-bold text-3xl md:text-4xl mb-6 tracking-wide">
                        ABOUT ME
                    </h2>
                    
                    <p class="text-gray-400 text-base md:text-lg leading-relaxed mb-10 text-left">
                        Halo, saya Annisa Tyas Wahyu Setyaningsih, seorang Frontend Developer yang berfokus pada pengembangan aplikasi web yang responsif dan user-friendly. Berpengalaman menggunakan React.js dan Flutter untuk membangun antarmuka modern, mengintegrasikan API, serta bekerja secara kolaboratif menggunakan Git dan Agile workflow.
                    </p>
                    
                    <div class="flex flex-wrap items-center gap-4 sm:gap-6">
                        <a 
                            href="/Tyas-CV-Frontend-Dev.pdf" 
                            target="_blank" 
                            rel="noopener noreferrer"
                            class="inline-block text-center px-8 md:px-10 py-3.5 rounded-lg text-white font-bold tracking-wider bg-linear-to-r from-blue-500 to-indigo-500 hover:scale-105 hover:shadow-[0_0_20px_rgba(56,189,248,0.3)] transition-all duration-300"
                        >
                            RESUME
                        </a>
                        
                    </div>
                </div>

            </div>
        </div>
    </section>
</template>

<script setup>

</script>