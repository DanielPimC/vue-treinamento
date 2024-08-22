<template>
    <div>
        <img :src="avatar" :alt="descricao">
    </div>
</template>

<script>
    export default {
        name: 'Picture',
        data() {
            return {
                avatar: "/img/user-icon.jpg",
                descricao: "Imagem de user"
            }
        }
    }
</script>

<style>
    img {
        width: 100px;
        height: 100px
    }
</style>