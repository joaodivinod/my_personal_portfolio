<script>
export default {
  name:'AboutMe'
}
</script>
<template>
  <section class="about">
    <div class="personal_container md:pt-28 pt-16 pb-16 md:pb-28 m-auto">
      <div class="flex about-itens">
        <div class="flex items-center">
          <font-awesome-icon icon="fa-solid fa-users"/>
          <h3 class="text-white font-bold ml-4">+ de 100 clientes</h3>
        </div>
        <div class="flex items-center">
          <font-awesome-icon icon="fa-solid fa-certificate" />
          <h3 class="text-white font-bold ml-4">+ de 5 anos experiencia</h3>
        </div>
        <div class="flex">
          <font-awesome-icon icon="fa-solid fa-rocket" />
          <h3 class="text-white font-bold ml-4">+ de 50 projetos</h3>
        </div>
      </div>
      <div class="about-info flex md:flex-row flex-col text-white md:mt-20 mt-12">
        <div class="md:basis-2/6 flex justify-start items-center ">
          <h2 class="font-bold md:text-left text-center md:mb-0 mb-6">Olá meu nome é <br class="md:flex hidden"> João Divino saiba <br class="md:flex hidden"> mais sobre mim</h2>
        </div>
        <div class="md:basis-4/6">
        <p>sou um desenvolvedor web com vasta experiência em diversos formatos de páginas, incluindo apresentação de produtos, sites de lançamento, páginas de educação a distância, entre outras. Também trabalhei em projetos de pessoas e empresas famosas e possuo prática em colaborar com times em projetos escaláveis e performáticos.</p>
        <p>Sou apaixonado pelo que faço e utilizo as melhores e mais recentes tecnologias do mercado para garantir que o seu projeto seja entregue exatamente como o previsto no layout inicial, dentro do prazo estipulado e com um preço justo.</p>
        <p>Meus objetivos profissionais incluem sempre me manter atualizado com as últimas tendências e tecnologias no desenvolvimento web, e continuar entregando soluções eficientes e inovadoras para meus clientes. O que me inspira e motiva nessa área é a possibilidade de criar algo que possa ser usado por muitas pessoas e que faça a diferença em suas vidas.</p>
        <p>Estou animado em colaborar com você e transformar sua ideia em realidade. Vamos trabalhar juntos e levar seu projeto para o próximo nível!</p>
        </div>
      </div>
    </div>
  </section>
</template>
<style lang="scss">
.about {
  background-color: #110C22;
  &-itens{ justify-content: space-between; & h3 { font-size: 28px; } }
  &-info{ & h2 { font-size: 48px; line-height: 53px; } }
}
.fa-users{ color: #DFA85B; font-size: 40px; }
.fa-certificate{ color: #7B7CF1; font-size: 40px; }
.fa-rocket{ color: #AF4889; font-size: 40px; }

  @media screen and (max-width: 1400px) {
    .about-info h2 { font-size: 40px; }
    .about-info p { font-size: 15px; }
  }
  @media screen and (max-width: 1100px) { .about-info h2 { font-size: 35px; } }
  @media screen and (max-width: 900px) { .about-info h2 { font-size: 28px; } }
  @media screen and (max-width: 800px) {
  .fa-users{ font-size: 30px; }
  .fa-certificate{ font-size: 30px; }
  .fa-rocket{ font-size: 30px; }

  .about{
    & h3 { font-size: 18px; }
  }
  }
  @media screen and (max-width: 767px) {
  .fa-users{ font-size: 20px; }
  .fa-certificate{ font-size: 20px; }
  .fa-rocket{ font-size: 20px; }

  .about{
    & h3 { font-size: 14px; }
    &-info{
      & h2{
        font-size: 20px;
        line-height: 30px;
      }
    }
  }
  }
  @media screen and (max-width: 390px) {
    .about{
      &-itens{
        flex-direction: column;
        & div{
          margin-top: 20px;
        }
      }
    }
  }
</style>