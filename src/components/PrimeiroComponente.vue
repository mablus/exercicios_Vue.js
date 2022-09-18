<template>
<div>
    <h1>Hola Vue!</h1>
    <p>Meu nome é {{ nome }} profissionalmente {{profissão}}</p>
    <MultiplosEventos/>
    <Reutilizacao/>
</div>
</template>

<script>
import MultiplosEventos from './MultiplosEventos';
import Reutilizacao from './Reutilizacao.vue';
    export default {
        name: 'Primeiro Componente',
        components:{
            MultiplosEventos,
            Reutilizacao
        },
        data(){
            return{
                nome:"Brito",
                profissão:"sofredor"

            }
        }
    }
</script>
