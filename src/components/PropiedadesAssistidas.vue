<!-- 
  PROPRIEDADES ASSISTIDAS:

  Demonstra o uso de watchers (propriedades assistidas) no Vue.js.
  Monitora mudanças em propriedades específicas e executa ações quando elas mudam.
  Útil para realizar ações assíncronas ou complexas em resposta a mudanças de dados.
-->

<template>
  <div class="componente">
    <h1>Componente com Propiedades Assistidas</h1>
    <p>Idade: {{ idade }}</p>
    <label>Ano do Nascimento: </label>
    <input type="number" v-model="anoNascimento" min="1900" />
    <label>Ano Atual: </label>
    <input type="number" v-model="anoAtual" min="2000" />
  </div>
</template>

<script setup>
import { ref } from "vue";
//import { watch } from "vue";
import { watchEffect } from "vue";

const anoNascimento = ref(1900);
const anoAtual = ref(2000);
const idade = ref(0);

/*
watch(anoAtual, (anoRecebidoParametro) => {
  idade.value = anoRecebidoParametro - anoNascimento.value;
});
watch(anoNascimento, (anoRecebidoParametro) => {
  idade.value = anoAtual.value - anoRecebidoParametro;
});

*/

watchEffect(() => {
  idade.value = anoAtual.value - anoNascimento.value;
});
</script>

<style scoped>
label {
  margin: 10px;
}
</style>
