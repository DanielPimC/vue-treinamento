<template>
    <div>
        <h2>Esta é a descrição da pessoa: {{ nome }}.</h2>
        <Info :email="email" :esta_trabalhando="esta_trabalhando"/>
    </div>
</template>

<script>
    import Info from './Info.vue'
    export default {
        name: 'Pessoa',
        components: {
            Info
        },
        data() {
            return {
                nome: 'Daniel',
                email: "daniel@email.com",
                esta_trabalhando: true
            }
        }     
    }
</script>