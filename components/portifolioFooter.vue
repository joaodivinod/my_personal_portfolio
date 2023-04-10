<script>
export default {
  name: 'PortifolioFooter',
  computed: {
    currentYear () {
      const year = new Date().getFullYear();
      return year.toString();
    }
  },
}
</script>
<template>
  <footer class="flex flex-col justify-center items-center">
  <div class="flex personal_container justify-center items-center pt-8 pb-8 m-auto">
    <a href="https://www.linkedin.com/in/jo%C3%A3o-divino/" target="blank" class="mr-4">
      <img src="../assets/img/linkedin.svg" alt="">
    </a>
    <a href="https://github.com/joaodivinod" target="blank">
      <img src="../assets/img/github.svg" alt="">
    </a>
  </div>
  <span class="text-white opacity-75 text-center md:mt-2 mt-4 mb-4">Criado por - João Divino · {{ currentYear }}</span>
  </footer>
</template>
<style lang="scss">
footer{
  background: #14142A;
  & a { transition: 500ms; &:hover{ transform: scale(1.1); } }
}
</style>