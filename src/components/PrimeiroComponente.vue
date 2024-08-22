<template>
    <div>
        <h1>Olá, Vue!</h1>
        <p>Meu nome é {{ nome }}, e tenho {{ idade }} anos.</p>
        <MultiplosEventos />
        <Reutilizacao />
        <Reutilizacao />
    </div>
</template>

<script>
    import MultiplosEventos from './MultiplosEventos.vue'
    import Reutilizacao from './Reutilizacao.vue'
    export default {
        name: 'PrimeiroComponente',
        components: {
            MultiplosEventos, 
            Reutilizacao
        },
        data() {
            return {
                nome: "Daniel",
                idade: 20
            }
        }
    }
</script>