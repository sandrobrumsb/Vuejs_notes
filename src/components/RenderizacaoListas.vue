<!-- 
  RENDERIZAÇÃO DE LISTAS:

  Demonstra como renderizar listas de elementos usando a diretiva v-for.
  Permite iterar sobre arrays e objetos para criar elementos repetitivos.
  Muito útil para exibir coleções de dados, como listas, tabelas e grids.
-->

<template>
  <div class="componente">
    <h1>Componente com Renderezação de Lista</h1>
    <p>Nome: {{ nome }}</p>
    <p v-show="cachorros.length === 0">Não tem cachorros</p>
    <ul>
      <!--v-for: pra cada cachorros em cachorros = vou gerar um li que cvai ter um nome e idade:-->
      <li v-for="cachorros in cachorros">
        Nome: {{ cachorros.nome }} | Idade: {{ cachorros.idade }}
      </li>
    </ul>
  </div>
</template>

<script setup>
import { defineProps } from "vue";

defineProps({
  nome: String,
  cachorros: Array,
});
</script>

<style scoped>
ul {
  margin: 0px;
  padding: 0px;
}

li {
  list-style: none;
  text-align: center;
  font-size: larger;
}
</style>
