<template>
    <div>
        <h1>Olá, Vue!</h1>
        <p>Meu nome é {{ nome }}, e tenho {{ idade }} anos.</p>
    </div>
</template>

<script>
    export default {
        name: 'PrimeiroComponente',
        data() {
            return {
                nome: "Daniel",
                idade: 20
            }
        }
    }
</script>