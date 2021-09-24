<template>
<div>
  <Header :esta_logado="false"/>
  <body>
    <PrimeiroComp />
    <p>O dado de teste é: {{ dado }}</p>
    <LifeCycle />
    <Pessoa />
  </body>
</div>
</template>

<script>
import PrimeiroComp from './components/PrimeiroComp.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/pessoa.vue'
import Style from './components/Style.vue'
import Header from './components/Header.vue'

  export default{
    name: "App",
    components: {
        PrimeiroComp,
        LifeCycle,
        Pessoa,
        Style,
        Header
    },

    data() {
      return{
        dado: "Teste"
      }
    }
  }
</script>

<style>
  body{
    background-color: #333;
    color: #FFF;
  }

  a {
    color: red;
  }

  .teste{
    background-color: #000;
  }
</style>

