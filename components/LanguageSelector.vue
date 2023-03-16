<template>
<section>

<div class="">
  <div>
    <div  @click="toggleDropdown">
      <img :src="selectedFlag" class="w-24">
    </div>
  </div>

  <div v-show="showDropdown">
    <div class="py-1" role="none">
      <div v-for="(language, index) in locales" :key="index" @click="selectLanguage(language)"> 
        <img class="w-24" :src="language.flag" alt="">
      </div>
    </div>
  </div>
</div>
</section>
</template>

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
  const objetoEncontrado = locales.find(objeto => objeto.code === this.$i18n.locale);
  this.selectedFlag = objetoEncontrado?.flag ?? '';
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

<style lang="sass">
.language-dropdown
  position: relative
  display: inline-block
  font-family: Arial, Helvetica, sans-serif
  cursor: pointer

.selected-language
  display: flex
  align-items: center
  padding: 0.5rem
  background-color: #7289da
  color: white

  img
    margin-right: 0.5rem
    height: 1rem

ul
  list-style-type: none
  margin: 0
  padding: 0
  position: absolute
  z-index: 1
  top: 100%
  left: 0
  right: 0
  background-color: #fff
  border-radius: 0.5rem
  box-shadow: 0 2px 4px rgba(0, 0, 0, 0.2)

li
  display: flex
  align-items: center
  padding: 0.5rem
  color: #333
  font-weight: bold
  transition: background-color 0.2s

  img
    margin-right: 0.5rem
    height: 1rem

  &:hover
    background-color: #f1f1f1
</style>
