<template>
  <header class="main-container main_header">
    <div class="main_header-info">
      <h2 class="font-bold">👋 Saudações!</h2>
      <h1 class="text-white font-bold">João Divino</h1>
      <h3>Frontend Developer Analyst</h3>
    </div>
    <div class="main_header-avatar">
      <img src="../assets/img/new_avatar.svg" alt="" />
    </div>
    <div>
      <div class="main_header-contact">
        <h4>Baixar cv</h4>
        <button>Vamos conversar</button>
      </div>
    </div>
  </header>
</template>
<script>
export default {
  name: 'MainHeader',
}
</script>
<style lang="scss">
.main_header {
  margin-top: 50px;
  display: flex;
  width: 100%;
  justify-content: center;
  align-items: center;
  &-info {
    & h1 { font-size: 3.25rem; }
    & h2 {
      color: var(--medium-purple);
      background-color: rgba(122, 74, 226, 0.1);
      padding: 8px;
      border-radius: 17px;
      width: 9rem;
    }
    width: 20%;
  }
  &-avatar {
    width: 60%;
    display: flex;
    justify-content: center;
    align-items: center;
    & img {
      width: 40%;
    }
  }
  &-contact { width: 20%; }
}
</style>
