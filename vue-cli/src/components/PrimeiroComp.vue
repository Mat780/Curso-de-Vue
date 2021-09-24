<template>
    <div>
        <h1>Olá vue</h1>
        <p>Meu nome é {{ name }} e estudo para ser um {{ job }}.</p>
    </div>
</template>

<script>
    export default{
        name: "PrimeiroComp",
        data() {
            return{
                name: "Matheus",
                job: "Programador"
            }
        }
    }
</script>
