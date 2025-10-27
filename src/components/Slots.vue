<!-- 
 SLOTS:

  Slots no Vue.js são espaços vazios dentro de um componente onde você pode colocar conteúdo personalizado quando usa esse componente. 
  É como um molde com buracos, e você escolhe o que vai dentro desses buracos cada vez que usa o molde.
  Assim, você reaproveita o mesmo componente, mas muda o conteúdo interno quando quiser.
-->

<template>
  <div class="componente">
    <h1>Componente com Slots:</h1>
    <button><slot name="texto" /> <slot name="icone" /></button>
    <button><slot name="icone" /> <slot name="texto" />Button</button>
  </div>
</template>
