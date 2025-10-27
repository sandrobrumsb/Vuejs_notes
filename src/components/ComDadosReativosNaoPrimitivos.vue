<!-- 
  DADOS REATIVOS NÃO PRIMITIVOS:

  Demonstra a reatividade do Vue.js com objetos e arrays (tipos não primitivos).
  Mostra como o Vue gerencia a reatividade em estruturas de dados complexas.
  Ilustra a atualização automática da interface ao modificar propriedades de objetos.
-->

<template>
  <div class="componente">
    <h1>componente com dados reativos nao Primitivos</h1>
    <p>Nome: {{ pessoa.nome }} | Idade: {{ pessoa.idade }}</p>
    <button @click="fazerAniversario()">Fazer aniversario</button>
    <!--v-on:click á a mesma coisa que @click-->
    <button @click="mudarNome()">Mudar nome</button>
  </div>
</template>

<!--Usando função setup api: 

<script setup>
import { reactive } from "vue"; // Aqui eu importo a função que diz ao view que essa Variavel pode mudar de valor.

const pessoa = reactive({ nome: "Sandro", idade: 36 });

function fazerAniversario() {
  pessoa.idade += 1; //.value permite alterar o conteudo da propriedade ref()
}

function mudarNome() {
  pessoa.nome = "Uzumaki Naruto";
}
</script>
-->

<!--Usando função Options api:-->
<script>
export default {
  data: function () {
    return {
      pessoa: {
        nome: "Sandro",
        idade: 27,
      },
    };
  },
  methods: {
    fazerAniversario: function () {
      this.pessoa.idade += 1;
    },
    mudarNome: function () {
      this.pessoa.nome = "Uchiha Sasuke";
    },
  },
};
</script>
