<!-- 
  COMPONENTE COM PROPS:

  Demonstra como passar dados entre componentes pai e filho usando props.
  Props são propriedades customizáveis que um componente pode receber.
  Fundamental para criar componentes reutilizáveis e modulares.
-->

<template>
  <div class="componente">
    <h1>Componente com props</h1>
    <p>{{ item }} (R$:{{ preco.toFixed(2) }})</p>
    <!--.toFixed(2) :  pra mostrar +2  casas decimal do numero-->
  </div>
</template>

<script setup>
import { defineProps } from "vue";
defineProps({
  item: String,
  preco: Number,
});
</script>
