# Introdução ao Vue.js

Este projeto contém exemplos práticos dos principais conceitos do Vue.js 3, implementados como componentes individuais.

## Estrutura do Projeto:

Comando usado para criar um novo projeto Vue.js
```sh
npm create vue@latest
```

O projeto está organizado em componentes individuais na pasta `src/components/`, cada um demonstrando um conceito específico do Vue.js.

### ⚙️ `src/main.js`
Arquivo principal de inicialização da aplicação.  
Ele **informa ao Vite** como construir e montar o projeto Vue, definindo o ponto de entrada e carregando o componente raiz `App.vue`.


### 🧱 `src/App.vue`
Componente raiz do projeto.  
É dividido em três seções principais:
- `<script>` — define a lógica e os dados do componente.  
- `<template>` — estrutura visual e marcação HTML.  
- `<style>` — estilos aplicados ao componente (pode usar CSS, SCSS ou outro pré-processador).

## Conceitos Estudados:

### Fundamentos

- **Primeiro Componente**: Estrutura básica de um componente Vue.js
- **Componente com Dados**: Gerenciamento básico de dados em componentes

### Reatividade

- **Dados Reativos Primitivos**: Manipulação de tipos primitivos com reatividade
- **Dados Reativos Não Primitivos**: Trabalho com objetos e arrays reativos

### Propriedades e Comunicação

- **Props**: Passagem de dados entre componentes pai e filho
- **Eventos**:
  - Emissão de eventos (child-to-parent)
  - Escuta de eventos (parent handling)

### Renderização

- **Renderização Condicional**: Uso de v-if, v-else-if e v-else
- **Renderização de Listas**: Iteração com v-for

### Dados Avançados

- **Propriedades Computadas**: Cálculos dinâmicos baseados em dados
- **Propriedades Assistidas (Watchers)**: Monitoramento de mudanças em dados

### Reutilização de Conteúdo

- **Slots**: Injeção de conteúdo personalizado em componentes

## Configuração do Projeto:

### IDE Recomendado

[VSCode](https://code.visualstudio.com/)

## ⚙️ Instalação e Configuração do Projeto:

Siga os passos abaixo para configurar e iniciar o projeto Vue.js em seu ambiente local.

Para obter uma cópia local desse projeto, execute o comando abaixo no seu terminal do vscode:

```sh
git clone https://github.com/sandrobrumsb/Vuejs_notes.git
```

Depois, certifique-se de que o **Node.js** está instalado e atualizado.  
Execute o comando abaixo no terminal:

```sh
node -v
```
Em seguida no terminal instale as dependências **Node.js e JavaScript**
```sh
npm install
```

Inicie o projeto no modo de desenvolvimento:

```sh
npm run dev
```


