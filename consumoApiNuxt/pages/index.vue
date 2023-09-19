<template>
  <div class="home">
    <h1>Página Inicial</h1>
    <NuxtLink to="/produtos">Ver Produtos</NuxtLink>

    <div>
      <h3>Feito por Othon Gonzaga</h3>
    </div>
  </div>
</template>

<script>
export default {
  name: 'IndexPage'
}
</script>

<style>
.home {
  text-align: center;
  padding: 20px;
  background-color: #f5f5f5;
}

.home h1 {
  font-size: 36px;
  color: #333;
}
</style>