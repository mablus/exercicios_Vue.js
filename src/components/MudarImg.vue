<template>
<div>
<button @click="$emit('mudarImg')">Trocar imagem de perfil</button>
</div>
</template>
<script>
export default {
    name:'MudarImg',
    emits: ['mudarImg']
}
</script>