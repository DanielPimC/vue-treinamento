<template>
    <div>
        <form action="" @submit.prevent="enviarForm">
            <input type="text" v-model="name">
            <input type="text" v-model="email">
            <input type="submit" value="Enviar">
        </form>
    </div>
</template>

<script>
    export default {
        name: 'Form',
        data() {
            return {
            name: 'Daniel',
            email: 'daniel@email.com'
            }
        },
        methods: {
            enviarForm() {
                const name = this.name
                const email = this.email
                alert(`Formulário enviado por ${name}, ao email ${email}`)
            }
        }
    }
</script>