<!-- 
  DADOS REATIVOS PRIMITIVOS:

  Demonstra a reatividade do Vue.js com tipos de dados primitivos (strings, números, etc).
  Mostra como os dados são automaticamente atualizados na interface quando modificados.
  Exemplo prático de como eventos podem modificar dados reativos primitivos.
-->

<template>
  <div class="componente">
    <h1>componente com dados reativos Primitivos</h1>
    <p>Nome: {{ nome }} | Idade: {{ idade }}</p>
    <button v-on:click="fazerAniversario()">Fazer aniversario</button>
    <!--v-on:click á a mesma coisa que @click-->
    <button @click="mudarNome()">Mudar nome</button>
  </div>
</template>

<script setup>
import { ref } from "vue"; // Aqui eu importo a função que diz ao view que essa Variavel pode mudar de valor.
const nome = ref("Sandro"); // Em seguida eu envolvo os valores dentro da função ref().
const idade = ref(36);

function fazerAniversario() {
  idade.value += 1; //.value permite alterar o conteudo da propriedade ref()
}

function mudarNome() {
  nome.value = "Uzumaki Naruto";
}
</script>
