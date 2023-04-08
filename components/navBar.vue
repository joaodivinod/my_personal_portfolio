<template>
  <nav class="hidden md:flex text-white">
    <ul class="flex items-center">
      <li
        v-for="(item, index) in $t('nav')"
        :key="index"
        class="px-3 py-2 text-base font-medium leading-5 text-white hover:text-purple-600 cursor-pointer transition duration-300 ease-in-out"
        >
        {{item}}
      </li>
    </ul>
  </nav>
</template>

<script>
export default {
  name: 'NavBar'
}
</script>

<style>

</style>
