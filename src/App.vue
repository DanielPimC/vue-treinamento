<template>
  <div>
    <Header :esta_logado="esta_logado" />
    <Form />
    <PrimeiroComponente />
    <LifeCycle />
    <Pessoa />
  </div>
</template>

<script>
  import LifeCycle from './components/LifeCycle.vue'
  import Pessoa from './components/Pessoa.vue'
  import PrimeiroComponente from './components/PrimeiroComponente.vue'
  import Header from './components/Header.vue'
  import Form from './components/Form.vue'

  export default {
    name: 'App',
    components: {
      PrimeiroComponente,
      LifeCycle,
      Pessoa, 
      Header,
      Form
    },
    data(){
      return {
        esta_logado: true
      }
    }
  }
</script>

<style>
  body{
    background-color: #333;
    color: #FFF
  }

  a{
    color: red;
  }
</style>