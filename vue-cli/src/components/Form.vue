<template>
    <div>
        <h2>Meu Formulario:</h2>
        <form action="" @submit="enviarFormulario($event)">
            <div><input type="text" v-model="name"></div>
            <div><input type="text" v-model="email"></div>
            <div><Submit /></div>
        </form>
        <p>Conteudo</p>
        <p>Conteudo</p>
        <p>Conteudo</p>
    </div>
</template>

<script>
import InputForm from './form/InputForm.vue'
import Submit from './form/Submit.vue'
export default {
    name: "Form",

    components: { 
        InputForm,
        Submit
    },

    data() {
        return {
            name: "",
            email: ""
        }
    },

    methods: {
        enviarFormulario(e){

            e.preventDefault();

            const name = this.name;
            const email = this.email;

            console.log("Formulário Enviado!");
            console.log("O nome é: " + name);
            console.log("O email é: " + email);

            // Ajax para mandar para o banco de dados

        }
    },
}
</script>

<style scoped>
    p{
        margin: 150px;
    }
</style>