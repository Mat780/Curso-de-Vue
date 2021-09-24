<template>
<div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de novas oportunidades!</p>
    <p>Estou codando no momento.</p>
    <p>Utilizo as seguintes tecnologias:</p>
    <ul>
        <li>Python</li>
        <li>C#</li>
        <li>C</li>
        <li>HTML e CSS</li>
        <li>JavaScript</li>
    </ul>
    <div>
        <button @click="showEmail">{{ botao_email }}</button>
    </div>
    <p v-if="mostrarEmail">Mande um email para: {{ email }}</p>
    <p class="teste">Para acessar o google <a v-bind:href="google" target="_blank">basta clickar aqui</a></p>
    <Picture />
</div>
</template>

<script>
import Picture from './Picture.vue'

export default {
    name: "Info",

    components: {
        Picture
    },

    data() {
        return{
            esta_trabalhando: false,
            mostrarEmail: false,
            email: "m.felipe@ufms.br",
            google: 'https://google.com',
            botao_email: 'Mostrar email'
        }
    },

    methods: {
        showEmail() {
            this.mostrarEmail = !this.mostrarEmail
            if (!this.mostrarEmail){
                this.botao_email = 'Mostrar email'
            } else {
                this.botao_email = 'Ocultar email'
            }
        }
    }
}
</script>