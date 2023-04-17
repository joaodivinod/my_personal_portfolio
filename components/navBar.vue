<script>
export default {
  name: 'NavBar',
  methods: {
    goToSection(index) {
      if (index === 0) {
        const homeSection = document.getElementById('home');
        window.scrollTo({
          top: homeSection.offsetTop - 64,
          behavior: 'smooth'
        });
      } else if (index === 1) {
        const aboutSection = document.getElementById('about');
        window.scrollTo({
          top: aboutSection.offsetTop - 64,
          behavior: 'smooth'
        });
        
      } else if (index === 2) {
        const servicesSection = document.getElementById('skills');
        window.scrollTo({
          top: servicesSection.offsetTop - 64,
          behavior: 'smooth'
        });
      }
      else if (index === 3) {
        const servicesSection = document.getElementById('contact');
        window.scrollTo({
          top: servicesSection.offsetTop - 64,
          behavior: 'smooth'
        });
      }
      
    }
  }
}
</script>
<template>
  <nav class="hidden md:flex text-white w-full justify-center items-center pt-5 pb-5 bg-red-900 fixed">
    <ul class="flex items-center">
      <li
        v-for="(item, index) in $t('nav')"
        :key="index"
        class="px-3 py-2 text-base font-medium leading-5 text-white hover:text-purple-600 cursor-pointer transition duration-300 ease-in-out"
        @click="goToSection(index)"
      >
        {{item}}
      </li>
    </ul>
  </nav>
</template>
<style scoped>
html {
  scroll-behavior: smooth;
}
nav{
  margin-top: -64px;
  background: #090e16;
  z-index: 999;
}
.section-container {
  scroll-margin-top: 6rem;
}
</style>
