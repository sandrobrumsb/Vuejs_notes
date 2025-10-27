<!-- 
  EMISSÃO DE EVENTOS:

  Demonstra como um componente filho pode emitir eventos para o componente pai.
  Usa o método emit() para enviar dados e notificações para componentes superiores.
  Fundamental para comunicação entre componentes de baixo para cima (child-to-parent).
-->

<template>
  <div class="componente">
    <h1>Componente que Emite o Evento</h1>
    <p>{{ item }} (R$:{{ preco.toFixed(2) }})</p>
    <!--.toFixed(2) :  pra mostrar +2  casas decimal do numero-->
    <button @click="adicionar">Adicionar ao carrinho</button>
  </div>
</template>

<script setup>
import { defineProps, defineEmits } from "vue";

const props = defineProps({
  item: String,
  preco: Number,
});

const emit = defineEmits(["FoiAdicionado"]);

function adicionar(params) {
  emit("FoiAdicionado", props.preco); //Acessando o preco atraves de defineProps na variavel const props.
}
</script>
