<template>
<div>
  <PrimeiroComp />
  <p>O dado de teste é: {{ dado }}</p>
  <LifeCycle />
</div>
</template>

<script>
import PrimeiroComp from './components/PrimeiroComp.vue'
import LifeCycle from './components/LifeCycle.vue'

  export default{
    name: "App",
    components: {
        PrimeiroComp,
        LifeCycle
    },

    data() {
      return{
        dado: "Teste"
      }
    }
  }
</script>