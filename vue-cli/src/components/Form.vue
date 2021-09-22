<template>
    <div>
        <h2>Meu Formulario:</h2>
        <form action="">
            <div><InputForm /></div>
            <div><InputForm /></div>
            <div><Submit /></div>
        </form>
    </div>
</template>

<script>
import InputForm from './form/InputForm.vue'
import Submit from './form/Submit.vue'
export default {
    components: { 
        InputForm,
        Submit
    },
    name: "Form"
}
</script>