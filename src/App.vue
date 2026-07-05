<template >
    <div class="min-h-screen bg-[#0B1221] relative overflow-x-hidden">
      <Navbar />
      <Home />
      <About />
      <Skill />
      <Project />
      <Contact />
    </div>
</template>

<script>
import AOS from 'aos';
import 'aos/dist/aos.css';
import Navbar from './components/Navbar.vue';
import Home from './components/Home.vue';
import About from './components/About.vue';
import Skill from './components/Skill.vue';
import Project from './components/Project.vue';
import Contact from './components/Contact.vue';
import {ref, nextTick, onMounted } from 'vue';

export default {
  components : {
    Navbar,
    Home,
    About,
    Skill,
    Project,
    Contact,
  },
  setup() {
    const loading = ref(true);

    onMounted(async () => {
      await nextTick();

      AOS.init({
        duration: 800,
        once: false,
        offset: 100,
        easing: 'ease-in-out',
        mirror: true,
      });
      setTimeout( () => {
        loading.value = false;
      }, 800);
    });
    return {loading};
  }
}
</script>

<style>
html {
  scroll-behavior: smooth;
}
</style>