<template>
    <div>
    <button @click="primeiro($event)"> Ativar multiplos eventos</button>
        <p>{{multiplos_eventos}}</p>
    </div>
</template>
<script>

export default {
    name:'MultiplosEventos',
    data(){
        return {
             multiplos_eventos:""
        }
    },
    methods:{
        primeiro(e){
            this.multiplos_eventos = "Primeiro evento ativado"
        }
    }
   
}
</script>

<style scoped>
    div{
        margin: 100px;
    }
</style>