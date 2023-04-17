<script lang="ts">
import { defineComponent } from 'vue';
import locales from '~/locales/locales.js'

export default defineComponent({
  name: 'LanguageSelector',
  data() {
    return {
      showDropdown: false,
      selectedFlag: '',
      locales
    }
  },

  mounted() {
    // @ts-ignore
    const selectedLanguage = this.locales.find(objeto => objeto.code === this.$i18n.locale);
    this.selectedFlag = selectedLanguage?.flag ?? '';
  },

  methods: {
    toggleDropdown() {
      this.showDropdown = !this.showDropdown;
    },
    selectLanguage(language: { code: string; flag: string }) {
      // @ts-ignore
      this.$i18n.setLocale(language.code);
      this.selectedFlag = language.flag;
      this.showDropdown = false;
    },

    changeLanguage(lang: string) {
      // @ts-ignore
      this.$i18n.setLocale(lang);
    }
  },
});
</script>
<template>
  <section @mouseenter="toggleDropdown" @mouseleave="toggleDropdown">
    <div class="language_dropdown" >
      <div class="language_dropdown-selected_flag">
        <img :src="selectedFlag" class="w-24">
        <font-awesome-icon icon="fa-solid fa-caret-down" class="arrow-icon" />
      </div>
      <div v-show="showDropdown" class="language_dropdown-dropdown_list">
        <div
          v-for="(language, index) in locales" :key="index"
          class="language_dropdown-dropdown_list-dropdown-item"
          :class="{'selected-language': language.code === $i18n.locale}"
          @click="selectLanguage(language)"
        >
            <img :src="language.flag" class="w-24" alt="">
            <font-awesome-icon v-show="language.code === $i18n.locale" icon="fa-solid fa-check" class="check-icon" />
        </div>
      </div>
    </div>
  </section>
</template>
<style lang="scss">
.language_dropdown{
  z-index: 9999;
  position: absolute;
  right: 50px;
  width: 60px;
  cursor: pointer;
  top: 30px;

  &-selected_flag{
    height: 30px;
    background: #271E4B;
    border-radius: 6px 6px 0 0;
    display: flex;
    justify-content: center;
    align-items: center;
    & img{
      width: 24px;
      margin-right: 5px;
    }
  }

  &-dropdown_list{
    background: #271E4B;
    margin-top: 5px;
    padding-bottom: 5px;
    border-radius: 0 0 6px 6px;
      & img{
      width: 24px;
      margin-right: 5px;
    }
    &-dropdown-item{
      display: flex;
      align-items: center;
      transition: 300ms;
      padding: 5px 0 5px 12px;
      &:hover{
        background-color: #0e0922;
      }
    }
  }
}
.arrow-icon,
.check-icon {
  color: #fff;
  width: 9px;
}
.selected-language{
  background-color: #5f4ba1;
}

@media screen and (max-width: 767px) {
  .language_dropdown{
    right: 12px;
    width: 47px;
  }

  .language_dropdown-dropdown_list img {
    width: 19px;
    margin-right: 5px;
  }

  .language_dropdown-selected_flag img {
    width: 19px;
  }
}
</style>
