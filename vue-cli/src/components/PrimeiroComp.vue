<template>
    <div>
        <h1>Olá vue</h1>
        <p>Meu nome é {{ name }} e estudo para ser um {{ job }}.</p>
        <MultiplosEventos />
    </div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos.vue'
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
        }
    }
</script>
