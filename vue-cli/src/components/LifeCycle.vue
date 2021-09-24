<template>
    <h1>Meu nome é: {{ name }}</h1>
</template>

<script>
export default {
    name: "LifeCycle",
    data() {
        return {
            name: "Ainda não sei"
        }
    },
    created() {
        setTimeout(() => {
            this.name = "Giovanna"
        }, 1000)
        this.lifeCycle()
    },
    mounted() {   
        setTimeout(() => {
            this.name = "Matheus"
        }, 2000);
    },

    methods: {
        lifeCycle(){
            console.log("LifeCycle executou")
        }
    },
}
</script>