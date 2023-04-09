<script>
import LanguageSelector from '../components/LanguageSelector.vue'
import NavBar from '../components/navBar.vue'
import WhatsappButton from '../components/wb-button.vue'
export default {
  name: 'MainHeader',
  components: {
    LanguageSelector,
    NavBar,
    WhatsappButton
  },
}
</script>
<template>
  <header class="main_header personal_container mx-auto mt-16">
    <section class="main_header-navs">
      <LanguageSelector/>
      <NavBar/>
    <div class="md:hidden flex md:mt-5">
      <a href="https://www.linkedin.com/in/jo%C3%A3o-divino/" target="blank" class="md:mr-4">
        <img src="../assets/img/linkedin.svg" alt="">
      </a>
      <a href="https://github.com/joaodivinod" target="blank">
        <img src="../assets/img/github.svg" alt="">
      </a>
    </div>
    </section>
    <section class="flex flex-col md:flex-row items-center	">
      <div class="main_header-info basis-1/3">
        <h2 class="font-bold hidden md:flex">👋 {{$t('welcome')}}</h2>
        <h1 class="md:mt-6 text-white font-bold hidden md:flex mt-2">João<br> Divino</h1>
        <h3 class="md:mt-4 md:text-sm hidden md:flex">Frontend Developer Analyst</h3>
        <div class="hidden md:flex md:mt-5">
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
      <div class="main_header-info md:hidden flex w-full flex-col md:mt-0 mt-10">
        <h2 class="font-bold mr-auto">👋 {{$t('welcome')}}</h2>
        <h1 class="md:mt-6 text-white font-bold mt-2">João<br> Divino</h1>
        <h3 class="md:mt-4 md:text-sm mb-2">Frontend Developer Analyst</h3>
        <div class="hidden md:flex md:mt-5">
          <a href="https://www.linkedin.com/in/jo%C3%A3o-divino/" target="blank" class="md:mr-4">
            <img src="../assets/img/linkedin.svg" alt="">
          </a>
          <a href="https://github.com/joaodivinod" target="blank">
            <img src="../assets/img/github.svg" alt="">
          </a>
        </div>
      </div>
      <div class="main_header-contact font-semibold text-base basis-1/3 flex flex-col items-end mr-auto md:mr-0">
        <WhatsappButton/>
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
  &-navs{
    display: flex;
    justify-content: center;
    margin-bottom: 150px;
  }
@media screen and (max-width: 767px) {
  .main_header {
    &-navs{
      display: flex;
      justify-content: center;
      margin-bottom: 60px;
      a {
        margin-right: 16px;
      }
    }

    &-info {
      & h1 {
        font-size: 46px;
        line-height: 59px;
      }
    }

    &-avatar {
      & img {
        width: 90%;
      }
    }
  }

  .main_header-info h2 {
    padding: 5px;
    border-radius: 21px;
    width: 122px;
    font-size: 14px;
  }
}
}
</style>
