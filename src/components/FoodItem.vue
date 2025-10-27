<!-- 
  FOOD ITEM:

  Um componente de exemplo que demonstra a estrutura básica de um item de comida.
  Mostra como criar componentes reutilizáveis com props e dados simples.
  Útil como exemplo de componente para listagem de itens de menu ou cardápio.
-->

<template>
  <div>
    <h2>{{ name }}</h2>
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: "Apples",
      message: "I like apples",
    };
  },
};
</script>

<style></style>
