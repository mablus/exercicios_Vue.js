<template>
 <div>
    <p>{{email}}</p>
    <p v-if="esta_trabalhando">Estou trabalhando no momento em um app Vue</p>
    <p v-else>Estou agora trabalhando em outras tecnologias.</p>
    <p>Vantagens do Vue</p>
    <ul >
      <li v-for="(Vantagens, index) in Vantagens_vue" v-bind:key="index">{{Vantagens}}</li>
      <li>a mais</li>
    </ul>
        <p>Mais vantagens</p>
        <ul>
          <li v-for="(Vantagens,index) in Mais_vantagens" v-bind:key="index">
          {{Vantagens.vantagem }}</li>
        </ul>
    <div>
    <button @click="showEmail">{{textoBotao}}</button>
    </div>
    <p v-show="mostrar_email">Mande uma mensagem para {{email}}</p>
    <p class="teste">Para acessar meu portifólio <a v-bind:href="meu_link" target="blank"> basta clicar aqui</a></p>
    <Picture/>
 </div>
</template>

<script>
import  Picture from './Picture.vue'
  export default{
  name:'Info',
  components:{
    Picture
  },
  props:{
    email: String
  },
  data(){
    return {
        esta_trabalhando: false,
        mostrar_email: false,
        
        meu_link: 'https://github.com/mablus',
        textoBotao:"Mostrar e-mail",
        Vantagens_vue:['rapido','leve','pré-estruturado'],
        Mais_vantagens:[ {id: 1, vantagem: 'acessivel'},
                         {id: 2, vantagem: 'Versátil' },
                         {id: 3 , vantagem: 'Excelente desempenho'}   ]
        

        

    }
  },
  methods: {
    showEmail(){
        this.mostrar_email = !this.mostrar_email
        if(!this.mostrar_email){
            this.textoBotao = 'Mostrar email'
        }else{
            this.textoBotao = 'Esconder email'
        }
    }
  }
} 
</script>