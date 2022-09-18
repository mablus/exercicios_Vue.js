<template>
    <h1>Meu nome é: {{nome}}</h1>
</template>

<script>
export default {
  name: 'LifeCycle',
  data() {
    return{
        nome: 'Ainda não definido'
    }
   
    
  },
   created(){
    setTimeout(()=>{
        this.nome = "Fabio"
    },2000);
    this.lifeCycle()
   },
   mounted(){
    setTimeout(()=>{
        this.nome = "Pedro"
    },3000);
    this.lifeCycle()
},
methods:{
  lifeCycle(){
    console.log("Execultado")
  }
}
}
</script>
