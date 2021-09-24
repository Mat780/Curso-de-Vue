<template>
    <div>
        <img :src="avatar" :alt="descricao">
        <Reutilazacao />
    </div>
</template>

<script>
import Reutilazacao from './Reutilazacao.vue'
export default {
    name: 'Picture',
    components: { 
        Reutilazacao
    },
    
    data() {
        return{
            avatar: "/img/avatar.png",
            descricao: "Avatarzin"
        }
    },
    
}
</script>