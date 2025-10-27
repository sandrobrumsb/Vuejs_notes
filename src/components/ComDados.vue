<!-- 
  COMPONENTE COM DADOS:

  Introduz o conceito de dados (data) em componentes Vue.js.
  Demonstra como declarar e utilizar propriedades de dados dentro de um componente.
  Um exemplo básico de como os dados são gerenciados e exibidos no template.
-->

<template>
  <div>
    <h1>componente com dados</h1>
    <p>nome: {{ nomeProduto }} - {{ codigoProduto }}</p>
  </div>
</template>
<style scoped>
div {
  text-align: center;
  border: 2px solid rgb(10, 69, 04);
  background-color: #050d04;
  border-radius: 15px;
  margin: 30px;
  padding: 10px;
}
p {
  font-size: 1.2rem;
}
</style>

<script setup>
const nomeProduto = "Lapis";
const codigoProduto = "#7898888888";
//nao precisa de return nesse formato.
</script>

<!-- <script>
 
//option api:
export default {
  data: function () {
    return {
      nomeProduto: "Caderno",
      codigoProduto: "#321",
    };
  },
  
//composition api: nao é a forma mais comum
export default {
  setup: function () {
    const nomeProduto = "Lapis";
    const codigoProduto = "#789";
    return { nomeProduto, codigoProduto };
  },
};
</script>

!-->
