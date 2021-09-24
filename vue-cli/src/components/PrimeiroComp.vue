<template>
    <div>
        <h1>Olá vue</h1>
        <p>Meu nome é {{ name }} e estudo para ser um {{ job }}.</p>
        <MultiplosEventos />
        <Reutilizacao />
    </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
import Reutilizacao from './Reutilazacao.vue'
    export default{
        name: "PrimeiroComp",
        data() {
            return{
                name: "Matheus",
                job: "Programador"
            }
        },

        components: {
            MultiplosEventos,
            Reutilizacao,
        }
    }
</script>
