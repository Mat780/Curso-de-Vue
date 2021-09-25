<template>
    <div>
        <img :src="avatar" :alt="descricao">
        <MudarImg @mudarImagem="trocarImagem"/>
    </div>
</template>

<script>
import MudarImg from './MudarImg.vue'
import Reutilazacao from './Reutilazacao.vue'
export default {
    name: 'Picture',
    components: { 
        Reutilazacao,
        MudarImg
    },
    
    data() {
        return{
            avatar: "/img/avatar.png",
            descricao: "Avatarzin"
        }
    },

    methods: {
        trocarImagem(){
            this.avatar = "/img/avatar2.png"
        }
    },
    
}
</script>