<script>
export default {
  name:'WhatsappButton'
}
</script>
<template>
  <button class="flex mt-3 p-2 md:p-3 justify-center items-center">
    <font-awesome-icon icon="fa-brands fa-whatsapp" />
    <span class="opacity-70">{{$t('talk')}}</span>
  </button>  
</template>
<style lang="scss">
button {
  transition: 500ms;
  border: 1px solid var(--medium-purple);
  border-radius: 17px;
  width: 12rem;
  color: var(--medium-purple);

  &:hover{
    background: var(--medium-purple);
    color: #090E16;
  }
}
  .fa-whatsapp {
    font-size: 1.5rem;
    margin-right: 8px;
  }
  @media screen and (max-width: 767px) {
  button {
    width: 170px;
    & span{
      font-size: 14px;
    }
  }

.fa-whatsapp {
    font-size: 18px;
    margin-right: 8px;
  }
}
</style>
