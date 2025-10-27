<!-- 
  DATA BINDING:

  Demonstra os dois tipos principais de data binding no Vue.js:
  - One-Way (v-bind): Dados fluem apenas do componente para o template
  - Two-Way (v-model): Sincronização bidirecional entre o componente e o template
  Essencial para entender como os dados são vinculados e atualizados na interface.
-->

<template>
  <div class="componente">
    <h1>Componente com Data Binding</h1>
    <p>{{ valorOneWay }}</p>
    <p>{{ valor }}</p>
    <!--
      One-Way Data Binding: 
    -->
      <input type="text" v-bind:value="valorOneWay"></input>
    
    <!--Two-Way Data Binding:-->
    <input type="text" v-bind:value="valor" v-on:input="(e)=>valor = (e).target.value"></input>
    <!--abaixo a mesma coisa de cima porem com os atalhos dos Bindings:
        Nesse caso o v-bind virou : e o v-on virou @ -->
    <input type="text" :value="valor" @input="(e)=>valor = (e).target.value"></input>

    <!--Forma otimizada Two-Way Data Binding:-->
    <input type="text" v-model="valor" ></input>
    
  </div> 
</template>

<script setup>
import {ref} from "vue";
const valorOneWay = ref("One-Way Data Binding")
const valor = ref("Two-Way Data Binding")
</script>


<!--- NOTES:

one-way Data Binding: É quando pego o conteudo do javascript e jogo ele no html ou vice-versa.
two-way Data Binding: É quando pego o valor da variavel, jogo ela no input(html) e pego as alterações do html e retorno para a variavel javascript atualizando a variavel.  


v-bind:value="valor": Aqui o v-bind pede que a strings "valor" dentro de value seja entendido como uma variavel, que esta la dentro de <script>, e oque esta dentro dessa variavel sera mostrado dentro do input.

v-on:input="(e)=>valor = (e).target.value": v-on:input é o tipo de evento que quero, nesse caso input. | (e)=>valor = (e).target.value: Função que pega o evento(e) e atualiza a variavel valor que recebe o evento.target.value. 
OBS: se a propriedade reativa for pega dentro do <script> no vue entao o valor.value tem que estar no script. 

-->