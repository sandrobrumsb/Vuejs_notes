<!-- 
  RENDERIZAÇÃO CONDICIONAL:

  Demonstra como renderizar elementos HTML condicionalmente usando v-if, v-else-if e v-else.
  Permite mostrar ou ocultar elementos baseado em condições específicas.
  Fundamental para criar interfaces dinâmicas que respondem ao estado da aplicação.
-->

<template>
  <div class="componente">
    <h1>Componente com Renderezação Condicional</h1>
    <p>Nome: {{ nome }}</p>
    <p v-if="qtdeCachorros == 0">Não tem Cachorros</p>
    <p v-else-if="qtdeCachorros === 1">Tem um Cachorros</p>
    <p v-else>Tem muitos Cachorros</p>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

defineProps({
  nome: String,
  qtdeCachorros: Number,
});
</script>
