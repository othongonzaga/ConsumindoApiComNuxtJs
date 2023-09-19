<template>
    <div class="produtos">
      <h1>Lista de Produtos</h1>
      <ul>
        <li v-for="produto in produtos" :key="produto.id" class="produto">
            {{ produto.id }} - {{ produto.title }}
        </li>
      </ul>
      <NuxtLink to="/">Voltar para a Página Inicial</NuxtLink>
    </div>
  </template>
  
<script>
export default {
    data() {
    return {
      produtos: [],
    };
  },

    async fetch() {
    try {
      const response = await fetch('https://jsonplaceholder.typicode.com/posts?_limit=10');
      const data = await response.json();
      this.produtos = data;
    } catch (error) {
      console.error('Erro ao buscar produtos:', error);
    }
  },

  
}
</script>
<style>
.produtos {
  text-align: center;
  padding: 20px;
  background-color: #f9f9f9;
}

.produtos h1 {
  font-size: 30px;
  color: #333;
}

.produtos ul {
  list-style-type: none;
  padding: 0;
}

.produto {
  font-size: 20px;
  color: #555;
  margin: 10px 0;
  border: 1px solid #ddd;
  padding: 10px;
  background-color: #fff;
}
</style>