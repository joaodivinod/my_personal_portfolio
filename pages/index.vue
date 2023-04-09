<script lang="ts">
import Vue from 'vue'
import MainHeader from '../components/main-header.vue'
import CallToAction from '../components/call-to-action.vue'
import AboutMe from '../components/about-me.vue'
import TecSkills from '../components/Tec-skills.vue'
import LetsTalk from '../components/lets-talk.vue'
import PortifolioFooter from '../components/portifolioFooter.vue'
export default Vue.extend({
  name: 'IndexPage',
  components: { MainHeader, CallToAction, AboutMe, TecSkills, LetsTalk, PortifolioFooter }
})
</script>
<template>
  <section> <MainHeader/> <CallToAction/> <AboutMe/> <TecSkills/> <LetsTalk/> <PortifolioFooter/> </section>
</template>