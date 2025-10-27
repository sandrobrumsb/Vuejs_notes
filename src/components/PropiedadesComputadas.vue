<!-- 
  PROPRIEDADES COMPUTADAS:

  Demonstra o uso de propriedades computadas (computed properties) no Vue.js.
  São propriedades que calculam automaticamente valores baseados em outras propriedades.
  Útil para cálculos dinâmicos que dependem de múltiplos dados do componente.
-->

<template>
  <div class="componente">
    <h1>Componente com Propiedades computadas</h1>
    <p>Idade: {{ idade }}</p>
    <label>Ano do Nascimento: </label>
    <input type="number" v-model="anoNascimento" min="1900" />
    <label>Ano Atual: </label>
    <input type="number" v-model="anoAtual" min="2000" />
  </div>
</template>

<script setup>
import { ref, computed } from "vue";

const anoNascimento = ref(1900);
const anoAtual = ref(2000);
const idade = computed(() => {
  return anoAtual.value - anoNascimento.value;
});
</script>

<style scoped>
label {
  margin: 10px;
}
</style>
