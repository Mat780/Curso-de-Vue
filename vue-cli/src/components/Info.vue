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
    <p v-if="mostrarEmail">Mande um email para: {{ email }}</p>
    <p>Para acessar o google <a v-bind:href="google" target="_blank">basta clickar aqui</a></p>
    <Picture />
</div>
</template>

<script>
import Picture from './Picture.vue'
export default {
  components: { Picture },
    name: "Info",
    data() {
        return{
            esta_trabalhando: false,
            mostrarEmail: true,
            email: "m.felipe@ufms.br",
            google: 'https://google.com'
        }
    }
}
</script>