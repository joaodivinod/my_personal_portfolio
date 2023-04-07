<script>
export default {
  name:'NavBar'
}
</script>
<template>
  <nav>
    <ul>
      <li>Home</li>
      <li>Sobre mim</li>
      <li>Porifolio</li>
      <li>Habilidades</li>
      <li>Contato</li>
    </ul>
  </nav>
</template>
<style lang="scss">
nav {
  color: #fff;
  & ul {
    display: flex;
    & li{
      margin-right: 16px;
      font-weight: 400;
      &:hover{
        color: #7B4AE2;
        cursor: pointer;
        transition: 300ms;
        // font-weight: 600;
        text-rendering: optimizeLegibility;
        backface-visibility: hidden;
      }
    }
  }
}
@media screen and (max-width: 700px) {
  nav {
    display: none;
  }
}
</style>