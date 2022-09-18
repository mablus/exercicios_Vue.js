<template>
    <Header/>
    <PrimeiroComponente/>
    <p>O dado de app é {{testando}}</p>
    <LifeCycle/>
    <Pessoa/>
    
</template>

<script>
    import PrimeiroComponente from './components/PrimeiroComponente.vue'
    import LifeCycle from './components/LifeCycle.vue'
    import Pessoa from './components/Pessoa.vue'
    import Header from './components/Header.vue'


    export default {
        name: 'App',
        components: {
            Header,
            PrimeiroComponente,
            LifeCycle,
            Pessoa
            
          
               
        }, data(){
            return{
                testando: "Teste"
            }
        }
    }
</script>

<style>
  body{
    background-color: #333;
    color: #fff;
  }
  a {
    color:rgb(215, 103, 103);
  }
  .teste {
    background-color: black;
  }
</style>
