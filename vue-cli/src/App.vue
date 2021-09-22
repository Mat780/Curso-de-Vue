<template>
<div>
  <PrimeiroComp />
  <p>O dado de teste é: {{ dado }}</p>
  <LifeCycle />
  <Pessoa />
</div>
</template>

<script>
import PrimeiroComp from './components/PrimeiroComp.vue'
import LifeCycle from './components/LifeCycle.vue'
import Pessoa from './components/pessoa.vue'

  export default{
    name: "App",
    components: {
        PrimeiroComp,
        LifeCycle,
        Pessoa
    },

    data() {
      return{
        dado: "Teste"
      }
    }
  }
</script>