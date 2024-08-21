<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Não estou trabalhando no momento.</p>
        <p>Utilizo as seguintes tecnologias:</p>
        <ul>
            <li>JavaScript</li>
            <li>Python</li>
            <li>PHP</li>
        </ul>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
    </div>
</template>

<script>
    export default {
        name: 'Info',
        data() {
            return {
                esta_trabalhando: true,
                mostrar_email: true,
                email: "daniel@email.com"
            }
        }
    }
</script>