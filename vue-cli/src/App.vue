<template>
<div>
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

  export default{
    name: "App",
    components: {
        PrimeiroComp,
        LifeCycle,
        Pessoa,
        Style
    },

    data() {
      return{
        dado: "Teste"
      }
    }
  }
</script>


