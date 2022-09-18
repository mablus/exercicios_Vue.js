<template>
    <ul>
      <li><a href=" # "> Home </a></li>
      <li><a href=" # "> Projetos </a></li>
      <li><a href=" # "> Contatos </a></li>
    </ul>
    
</template>

<script>
export default {
    name:'Header'
}
</script>

<style scoped>
  ul{
    list-style: none;
    display:flex;
    transform: .5s;
  }
  a:hover {
    color:turquoise;
  }

  li {
    margin-right: 10px;
  }

  a {
    color: darkgoldenrod;
    text-decoration: none;
    transition: .5s;
  }

  a:hover {
    color: turquoise;
  }
</style>