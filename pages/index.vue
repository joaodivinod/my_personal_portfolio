<template>
  <MainHeader/>
</template>

<script lang="ts">
import Vue from 'vue'
import MainHeader from '../components/main-header.vue'
export default Vue.extend({
  name: 'IndexPage',
  components: {
    MainHeader
  }
})
</script>
