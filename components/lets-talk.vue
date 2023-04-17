<script>
import WhatsappButton from '../components/wb-button.vue'
export default {
  name: 'LetsTalk',
  components: {
    WhatsappButton
  },
  methods: {
    async copyText() {
      console.log('Chamou copyText')
      const text = 'joaodivinod@gmail.com';
      try {
        await navigator.clipboard.writeText(text);
        this.$refs.tooltip.classList.remove('hidden');
        setTimeout(() => {
          this.$refs.tooltip.classList.add('hidden');
        }, 2000);
      } catch (err) {
        console.log('Erro ao copiar o texto: ', err);
      }
    }
  }
}
</script>
<template>
  <section id="contact" class="talk personal_container relative">
  <h2>{{ $t('contact') }}</h2>
  <div class="flex md:flex-row flex-col justify-between items-center md:max-w-[500px] w-full">
    <WhatsappButton/>
    <div class="flex flex-col mt-10">
      <h3 class="mt-3">E-mail:</h3>
      <h4 class="text-white mb-5 opacity-50">joaodivinod@gmail.com</h4>
      <font-awesome-icon icon="fa-solid fa-copy" @click="copyText"/>
      <div ref="tooltip" class="tooltip hidden absolute bottom-0 left-1/2 transform -translate-x-1/2 animate-fadeIn">
      <font-awesome-icon icon="fa-solid fa-square-check" class="text-white mr-3" /> E-mail Copiado!
      </div>
    </div>
  </div>
  </section>
</template>

<style lang="scss">
.talk { @apply mt-12 md:mt-20 mb-20 mx-auto text-center flex flex-col items-center justify-center; }
.talk h2 { @apply text-white font-bold md:text-5xl text-2xl; }
.fa-paper-plane {
  color: var(--medium-purple);
  font-size: 1.5rem;
}
.fa-copy {
  font-size: 1.5rem;
  color: var(--medium-purple);
  cursor: pointer;
}
h3{
  color: #7B4AE2;
  font-size: 20px;
}
.tooltip {
  position: absolute;
  padding: 4px 8px;
  color: #fff;
  border-radius: 4px;
  z-index: 999;
  height: 40px;
  background: #422c7c;
  display: flex;
  justify-content: center;
  align-items: center;
  font-size: 16px;
  opacity: 0.5;
}

.tooltip.hidden {
  display: none;
}

.animate-fadeIn {
  animation-name: fadeIn;
  animation-duration: 0.5s;
  animation-fill-mode: forwards;
  opacity: 0;
}

.animate-fadeOut {
  animation-name: fadeOut;
  animation-duration: 0.5s;
  animation-fill-mode: forwards;
  opacity: 1;
}

@keyframes fadeIn {
  from { opacity: 0; bottom: -20px; }
  to { opacity: 1; bottom: 20px; }
}

@keyframes fadeOut {
  from { opacity: 1; bottom: 20px; }
  to { opacity: 0; bottom: -20px; }
}

@media screen and (max-width: 767px) {
  h3{
    font-size: 16px;
  }
}
</style>
