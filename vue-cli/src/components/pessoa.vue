<template>
<div>
    <h2>Esta é a descrição da pessoa: {{ name }}</h2>
    <Info :email="email" :esta_trabalhando="true" />
    <Form />
</div>
</template>

<script>
import Form from './Form.vue'
import Info from './Info.vue'
export default {
    name: "pessoa",
    components: { 
        Info,
        Form 
    },
    data() {
        return {
            name: "Matheus",
            email: "m.felipe@ufms.br"
        }
    }
}
</script>