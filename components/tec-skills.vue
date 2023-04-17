<script>
export default {
  name: 'TecSkills'
}
</script>
<template>
  <section id="skills" class="tec personal_container">
    <h2>{{ $t('skills') }}</h2>
    <img src="../assets/img/tecs.svg" alt="">
  </section>
</template>

<style lang="scss">
.tec { @apply mt-12 md:mt-20 mb-32 mx-auto text-center flex flex-col items-center justify-center; }
.tec h2 { @apply text-white font-bold md:text-5xl text-2xl; }
.tec img { @apply mt-12 md:mt-20 max-w-[70%] md:max-w-[35%]; }
</style>
