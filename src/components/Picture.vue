<template>
    <img :src="avatar" :alt="descricao">
    <MudarImg @mudar-img="mudarImg"/>
</template>
<script>
import MudarImg from './MudarImg.vue'
export default {
    name:'Picture',
    components:{
        MudarImg
    },
    data(){
        return{
            avatar: './img/avatar.png',
            descricao:'Imagem de usuario'
        }
    },
    methods: {
        MudarImg(){
            this.avatar = "/img/avatar2.png"
        }
    }
}
</script>