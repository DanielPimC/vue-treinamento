<template>
    <h1>Meu nome é: {{ nome }}</h1>
</template>

<script>
    export default{
        name: 'LifeCycle',
        data(){
            return {
                nome: 'Ainda não sei.'
            }
        },
        created() {
            setTimeout(() => {
                this.nome = 'Daniel'
                
            }, 1000)
        },
        mounted() {
            setTimeout(() => {
                this.nome = 'Joaquim'
            }, 2000)
        },
        methods: {
            lifeCycle() {
                console.log("executou")
            }
        }
    }
</script>