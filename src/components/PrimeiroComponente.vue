<!-- 
  PRIMEIRO COMPONENTE:

  Este é um exemplo básico de um componente Vue.js, demonstrando a estrutura fundamental de um componente.
  Mostra como criar um componente simples com template e estilo.
  É o ponto de partida para entender a componentização no Vue.js, exibindo uma mensagem básica "Hello World".
-->

<template>
  <div>
    <h1>Hello World</h1>
  </div>
</template>

/*scoped: aplica a formatação CSS somente nesse componente*/
<style scoped>
div {
  background-color: #0e7e28;
  padding: 20px;
  margin: 30px;
  border-radius: 5px;
  text-align: center;
}
div:hover {
  background-color: #13b939;
}

h1 {
  color: white;
  margin-bottom: 10px;
}
</style>
