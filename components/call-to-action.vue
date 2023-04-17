<script>
export default {
  name:'CallToAction'
}
</script>
<template>
 <section class="ideas flex flex-col items-center">
  <div class="personal_container text-center pt-20 pb-20 flex flex-col text-white">
    <h1 class="font-bold">{{ $t('lifeHeader') }}</h1>
    <p class="opacity-50 md:mt-1 mt-2">{{ $t('lifeText') }}</p>
  </div>
 </section>
</template>
<style lang="scss">
  .ideas{
    margin-top: 200px;
    background-color: #443672;
    & h1{
      font-size: 48px;
    }
  }
  @media screen and (max-width: 767px) {
    .ideas{ margin-top: 100px; & h1{ font-size: 38px; } & p { font-size: 16px; } }
  }
  @media screen and (max-width: 600px) {
    .ideas{ margin-top: 100px; & h1{ font-size: 25px; } & p { font-size: 14px; } }
}
</style>
