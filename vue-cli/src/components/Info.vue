<template>
<div>
    <p v-if="esta_trabalhando">Estou trabalhando no momento</p>
    <p v-else>Estou em busca de novas oportunidades!</p>
    <p>Estou codando no momento.</p>
    <p>Utilizo as seguintes tecnologias para Back-End:</p>
    <ul>
        <li v-for="(technology, index) in backend_tech" v-bind:key="index">
            {{ technology }}
        </li>
    </ul>
    <p>Utilizo as seguintes tecnologias para Front-End:</p>
    <ul>
        <li v-for="technology in frontend_tech" :key="technology.id">
            {{ technology.language }}
        </li>
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
            botao_email: 'Mostrar email',
            backend_tech: ['JavaScript', 'Python', 'C', 'C#'],
            frontend_tech: [
                {id: 1, language: 'HTML'},
                {id: 2, language: 'CSS'},
                {id: 3, language: 'Vue'}
            ]
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