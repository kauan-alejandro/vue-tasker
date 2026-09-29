# Vue Tasker - Seminário Vue.js

## Objetivo
Criar um gerenciador de tarefas (Vue Tasker) interativo, executado no navegador, para demonstrar na prática os conceitos fundamentais do Vue.js (SFC, reatividade e diretivas).

## Integrantes
Ana Carolina Gonçalves, Cassiano Luiz brandes soares, Davi Ferreira da Cunha, Enrico Augusto Pereira Naba, Guilherme Emanuel Gonçalves, João Vitor Charleaux, Kauan Alejandro da Rosa, Luana Gabrielle Ferreira Guedes Paes, Pedro Augusto Lombardi da Costa, Rodrigo Santos Graça, Victor Luiz Koba Batista.
**Turma:** 2º Análise e Desenvolvimento de Sistemas - Noite.

## Tecnologia e Versão
* Vue.js 3 (Composition API)
* Vite

## Pré-requisitos
* Node.js 20.19 ou superior
* npm

## Instalação
1. Clone o repositório: `git clone https://github.com/kauan-alejandro/vue-tasker.git`
2. Acesse a pasta: `cd vue-tasker`
3. Instale as dependências: `npm install`

## Execução
Execute o servidor local com o comando:
`npm run dev`
Acesse no navegador: `http://localhost:5173`

## Estrutura do Projeto
* `src/App.vue`: Componente raiz (Root) que envolve a aplicação e contém a lógica da lista de tarefas.
* `src/main.js`: Ponto de entrada JS; instancia e monta o Vue na DOM.

## Funcionalidades
* Adicionar novas tarefas.
* Marcar tarefas como concluídas.
* Remover tarefas da lista.

## Vulnerabilidade Pesquisada
* **Identificador:** CVE-2024-6783
* **Componente:** vue-template-compiler (Afeta projetos que ainda utilizam o Vue.js 2.x)
* **Tipo:** Client-side Cross-Site Scripting (XSS) via Prototype Pollution
* **Impacto:** Permite que um invasor injete e execute códigos JavaScript arbitrários no navegador do usuário.
* **Mitigação:** Migrar a aplicação para o Vue 3, que já possui essa falha corrigida nativamente.

## Evidências / Imagens
<img width="1917" height="967" alt="print-projeto" src="https://github.com/user-attachments/assets/3852268d-98d8-4067-a724-31b1309c83e3" />


## Link do GitHub Pages
Acesse a aplicação a funcionar aqui: https://kauan-alejandro.github.io/vue-tasker/

## Referências
* https://vuejs.org/guide/scaling-up/sfc.html
* https://vuejs.org/guide/extras/reactivity-in-depth.html
