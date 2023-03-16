<script>
import LanguageSelector from '../components/LanguageSelector.vue'
export default {
  name: 'MainHeader',
  components: {
    LanguageSelector
  },
}
</script>
<template>
  <header class="main_header container mx-auto mt-16">
    <LanguageSelector/>
    <nav>
      <span>Aqui vai ter um menu</span>
    </nav>
    <section class="flex flex-row items-center	">
      <div class="main_header-info basis-1/3">
        <h2 class="font-bold">👋 Saudações!</h2>
        <h1>{{ $t('welcome') }}</h1>
        <!-- <router-link :to="{ path: switchLocalePath('fr') }">fr</router-link>
        <router-link :to="{ path: switchLocalePath('en') }">en</router-link>
        <router-link :to="{ path: switchLocalePath('pt-br') }">pt</router-link>
        <router-link :to="{ path: switchLocalePath('es') }">Es</router-link> -->
        <h1 class="md:mt-6 text-white font-bold">João <br> Divino</h1>
        <h3 class="md:mt-4 md:text-sm">Frontend Developer Analyst</h3>
        <div class="flex md:mt-5">
          <a href="https://www.linkedin.com/in/jo%C3%A3o-divino/" target="blank" class="md:mr-4">
            <img src="../assets/img/linkedin.svg" alt="">
          </a>
          <a href="https://github.com/joaodivinod" target="blank">
            <img src="../assets/img/github.svg" alt="">
          </a>
        </div>
      </div>
      <div class="main_header-avatar basis-2/3">
        <img src="../assets/img/new_avatar.svg" alt="" />
      </div>
      <div class="main_header-contact font-semibold text-base basis-1/3 flex flex-col items-end">
        <a href="#" class="flex hover:text-purple-500	items-center">
          <h4 class="mr-1 opacity-70">Baixar cv</h4>
          <font-awesome-icon icon="fa-solid fa-cloud-arrow-down" />
        </a>
        <button class="flex mt-3 p-3 ">
          <font-awesome-icon icon="fa-brands fa-whatsapp" />
          <span class="opacity-70">Vamos conversar</span>
        </button>
      </div>
    </section>
  </header>
</template>
<style lang="scss">
.main_header {
  &-info {
    & h1 {
      font-size: 3.25rem;
      line-height: 4rem;
    }
    & h2 {
      color: var(--medium-purple);
      background-color: rgba(122, 74, 226, 0.1);
      padding: 8px;
      border-radius: 17px;
      width: 9rem;
    }

    & h3 { color: #fff; opacity: 0.5; }

    & a { transition: 500ms; &:hover{ transform: scale(1.1); } }
  }
  &-avatar {
    display: flex;
    justify-content: center;
    align-items: center;
    & img {
      width: 70%;
    }
  }
  &-contact {
    color: var(--medium-purple);

    & button {
      transition: 500ms;
      border: 1px solid var(--medium-purple);
      border-radius: 17px;
      width: 12rem;

      &:hover{
        background: var(--medium-purple);
        color: #090E16;
      }
    }
  }
}
</style>
