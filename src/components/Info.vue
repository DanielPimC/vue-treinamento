<template>
    <div>
        <p v-if="esta_trabalhando">Estou trabalhando no momento.</p>
        <p v-else>Não estou trabalhando no momento.</p>
        <p>Utilizo as seguintes tecnologias para back-end:</p>
        <ul>
            <li v-for="(tecnologia, index) in tecnologias_back" :key="index">{{ tecnologia }}, {{ index }}</li>
        </ul>
        <p>Utilizo as seguintes tecnologias para front-end:</p>
        <ul>
            <li v-for="(tecnologia, id) in tecnologias_front" :key="id">{{ tecnologia.nome }}, {{ tecnologia.id }}</li>
        </ul>
        <div>
            <button @click="showEmail">{{ texto_botao }}</button>
        </div>
        <p v-show="mostrar_email">Mande uma mensagem para: {{ email }}</p>
        <p>Para ver o portfolio, <a :href="meu_link" target="_blank">Clique aqui </a></p>
        <Picture />
    </div>
</template>

<script>
    import Picture from './Picture.vue';
    export default {
        name: 'Info',
        components: {
            Picture   
        },
        props: {
            email: String,
            esta_trabalhando: Boolean
        },
        data() {
            return {
                mostrar_email: false,
                meu_link: 'https://google.com',
                texto_botao: 'Exibir email do usuário',
                tecnologias_back: ['JavaScript', 'Python', 'PHP'],
                tecnologias_front: [
                    {id: 1, nome: 'HTML'},
                    {id: 2, nome: 'CSS'},
                    {id: 3, nome: 'JavaScript'}
                ]
            }
        },
        methods: {
            showEmail() {
                this.mostrar_email = !this.mostrar_email
                if(!this.mostrar_email){
                    this.texto_botao = 'Exibir email'
                }else{
                    this.texto_botao = 'Ocultar email'
                }
            }
        }
    }
</script>