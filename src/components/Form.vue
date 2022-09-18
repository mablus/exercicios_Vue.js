<template>
  <div>
    <form action="" @submit="enviarFomulario($event)">
    <div>
    <input type="text" v-model="name">
    </div>
    <div>
    <input type="text" v-model="email">
    </div>
    <div>
    <submit/>
    </div>
    </form>
    <p>Conteúdo</p>
    <p>Conteúdo</p>
    <p>Conteúdo</p>
  </div>
</template>

<script>
import InputText from './form/InputText.vue'
import Submit from './form/Submit.vue'
export default {
    name: 'Form',
    components:{
        InputText,
        Submit
    },
    data(){
        return{
            name:"",
            email:""
        }
    },
    methods: {
        enviarFomrulario(e){
            e.preventDefault();

            const name = this.name;
            const email = this.email;

            console.log('formulário Enviado');
            console.log('O nome é'+ nome);
            console.log('O email é '+ email);
        }
    }
}
</script>

<style scoped>
    p {
        margin: 50px;
    }
</style>