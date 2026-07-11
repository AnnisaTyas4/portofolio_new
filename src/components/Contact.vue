<template>
  <section id="contact" class="relative w-full overflow-hidden bg-gradient-to-br from-[#3b2591] via-[#4d61c6] to-[#45a4d5] font-sans flex flex-col pt-10 md:pt-12 pb-6 px-5 sm:px-6 md:px-12 lg:px-20 scroll-mt-24 text-white">
    
    <div class="absolute -top-24 sm:-top-32 -left-24 sm:-left-32 w-[75vw] h-[75vw] max-w-[500px] max-h-[500px] bg-[#3a2099] rounded-full mix-blend-multiply filter blur-[80px] sm:blur-[100px] opacity-80 pointer-events-none z-0"></div>
    <div class="absolute top-0 right-0 w-[80vw] h-[80vw] max-w-[600px] max-h-[600px] bg-[#4ba1d2] rounded-full mix-blend-screen filter blur-[90px] sm:blur-[120px] opacity-40 pointer-events-none z-0"></div>

    <div class="relative z-10 w-full mb-8 sm:mb-10 lg:mb-16">
      <h2 
        class="text-center text-lg sm:text-xl md:text-2xl font-bold tracking-[0.18em] sm:tracking-[0.2em]"
        data-aos="fade-up"
      >
        CONTACT
      </h2>
    </div>

    <div class="relative z-10 grid lg:grid-cols-2 gap-10 lg:gap-12 max-w-6xl mx-auto w-full items-center">
      
      <div 
        class="flex flex-col justify-start lg:pl-16 min-w-0"
        data-aos="fade-right"
      >
        <h3 class="text-2xl sm:text-3xl md:text-4xl font-bold mb-4">Drop Me a Message</h3>
        <p class="text-blue-100/80 mb-8 max-w-md text-sm md:text-base leading-relaxed">
          Let's connect! If you have a job opportunity, project collaboration, or any questions about my experience and skills, feel free to reach out. I'd be happy to respond to your message.
        </p>

        <div class="space-y-5">
          <div class="flex items-center gap-3 sm:gap-5 min-w-0">
            <div class="w-10 h-10 sm:w-12 sm:h-12 rounded-xl bg-[#4b75e6] shadow-lg flex items-center justify-center shrink-0">
              <MapPinIcon class="w-5 h-5 text-white" />
            </div>
            <span class="text-blue-50 font-medium tracking-wide leading-relaxed text-sm sm:text-base min-w-0 break-words">
              Ungaran
            </span>
          </div>

          <div class="flex items-center gap-3 sm:gap-5 min-w-0">
            <div class="w-10 h-10 sm:w-12 sm:h-12 rounded-xl bg-[#4b75e6] shadow-lg flex items-center justify-center shrink-0">
              <PhoneIcon class="w-5 h-5 text-white" />
            </div>
            <span class="text-blue-50 font-medium tracking-wide text-sm sm:text-base min-w-0 break-words">+62 85727962535</span>
          </div>
          
          <div class="flex items-center gap-3 sm:gap-5 min-w-0">
            <div class="w-10 h-10 sm:w-12 sm:h-12 rounded-xl bg-[#4b75e6] shadow-lg flex items-center justify-center shrink-0">
              <EnvelopeIcon class="w-5 h-5 text-white" />
            </div>
            <span class="text-blue-50 font-medium tracking-wide text-sm sm:text-base min-w-0 break-all">anissatyas254@gmail.com</span>
          </div>
          
        </div>
      </div>

      <div 
        class="flex justify-center lg:justify-end items-start min-w-0"
        data-aos="fade-left"
      >
        <form @submit.prevent="submitForm" class="w-full max-w-md flex flex-col gap-6 mt-2">
          
          <div class="relative w-full">
            <input 
              type="text" 
              id="name"
              placeholder="Name" 
              class="peer w-full bg-transparent text-white placeholder-transparent px-0 py-2 outline-none transition-all border-none focus:ring-0"
            >
            <label 
              for="name"
              class="absolute left-0 -top-3.5 text-blue-200 text-xs transition-all pointer-events-none peer-placeholder-shown:text-gray-300 peer-placeholder-shown:text-base peer-placeholder-shown:top-2 peer-focus:-top-3.5 peer-focus:text-xs peer-focus:text-blue-200"
            >
              Name
            </label>
          </div>

          <div class="relative w-full">
            <input 
              type="email" 
              id="email"
              placeholder="Email" 
              class="peer w-full bg-transparent text-white placeholder-transparent px-0 py-2 outline-none transition-all border-none focus:ring-0"
            >
            <label 
              for="email"
              class="absolute left-0 -top-3.5 text-blue-200 text-xs transition-all pointer-events-none peer-placeholder-shown:text-gray-300 peer-placeholder-shown:text-base peer-placeholder-shown:top-2 peer-focus:-top-3.5 peer-focus:text-xs peer-focus:text-blue-200"
            >
              Email
            </label>
          </div>

          <div class="relative w-full">
            <textarea 
              id="message"
              rows="4" 
              placeholder="Message" 
              class="peer w-full bg-transparent text-white placeholder-transparent px-0 py-2 outline-none transition-all resize-none border-none focus:ring-0"
            ></textarea>
            <label 
              for="message"
              class="absolute left-0 -top-3.5 text-blue-200 text-xs transition-all pointer-events-none peer-placeholder-shown:text-gray-300 peer-placeholder-shown:text-base peer-placeholder-shown:top-2 peer-focus:-top-3.5 peer-focus:text-xs peer-focus:text-blue-200"
            >
              Message
            </label>
          </div>
          
          <div class="mt-4">
            <button 
              type="submit" 
              class="w-full sm:w-auto bg-[#4b75e6] hover:bg-[#3a5fc7] text-white font-bold tracking-wide py-3 px-8 rounded-xl transition-colors shadow-lg"
            >
              Send
            </button>
          </div>
        </form>
      </div>
    </div>

    <div 
      class="relative z-10 mt-10 border-t border-white/20 pt-6 flex justify-center items-center"
      
    >
      <p class="text-blue-100/70 text-xs sm:text-sm text-center">
        © Annisa Tyas All rights reserved
      </p>
    </div>
  </section>
</template>

<script setup>
import { 
  PhoneIcon, 
  EnvelopeIcon, 
  MapPinIcon 
} from '@heroicons/vue/24/solid';

const submitForm = () => {
  console.log('Form disubmit!');
};
</script>