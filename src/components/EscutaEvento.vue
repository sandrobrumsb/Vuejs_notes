<!-- 
  ESCUTA DE EVENTOS:

  Demonstra como um componente pai pode escutar e reagir a eventos emitidos por componentes filhos.
  Usa o v-on ou @ para capturar eventos personalizados dos componentes filhos.
  Complementa o sistema de comunicação child-to-parent do Vue.js.
-->

<template>
  <div class="componente">
    <h1>Esse Componetente que Escuta Evento</h1>
    <p>Total: R${{ total }}</p>
    <div class="lista">
      <EmiteEvento item="Item1" :preco="1.99" @FoiAdicionado="atualizarTotal" />
      <EmiteEvento
        item2="Item2"
        :preco="5.01"
        @FoiAdicionado="atualizarTotal"
      />
      <EmiteEvento
        item3="Item3"
        :preco="10.99"
        @FoiAdicionado="atualizarTotal"
      />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue"; // Importa a função 'ref' do Vue, que é usada para criar variáveis reativas
import EmiteEvento from "./EmiteEvento.vue"; // Importa um componente chamado EmiteEvento, que está em outro arquivo

const total = ref(0); // Cria uma variável reativa chamada 'total' e começa com o valor 0

// Define uma função chamada 'atualizarTotal' que recebe um valor 'p'
function atualizarTotal(p) {
  const valor = total.value + p; // Soma o valor atual de 'total' com 'p' e guarda na variável 'valor'

  total.value = +valor.toFixed(2); // Arredonda o valor para duas casas decimais e atualiza o 'total'
}
</script>

<style scoped>
.lista {
  display: flex;
  justify-content: space-between;
}
</style>
