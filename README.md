# Vue Tasker - Seminário Vue.js

## Objetivo
Criar um gerenciador de tarefas (Vue Tasker) interativo, executado no navegador, para demonstrar na prática os conceitos fundamentais do Vue.js (SFC, reatividade e diretivas)[cite: 1].

## Integrantes
Ana Carolina Gonçalves, Cassiano Luiz brandes soares, Davi Ferreira da Cunha, Enrico Augusto Pereira Naba, Guilherme Emanuel Gonçalves, João Vitor Charleaux, Kauan Alejandro da Rosa, Luana Gabrielle Ferreira Guedes Paes, Pedro Augusto Lombardi da Costa, Rodrigo Santos Graça, Victor Luiz Koba Batista[cite: 1].
**Turma:** 2º Análise e Desenvolvimento de Sistemas - Noite[cite: 1].

## Tecnologia e Versão
* Vue.js 3 (Composition API)
* Vite

## Pré-requisitos
* Node.js 20.19 ou superior[cite: 1]
* npm[cite: 1]

## Instalação
1. Clone o repositório: `git clone [COLOQUE_O_LINK_DO_SEU_REPOSITORIO_AQUI]`
2. Acesse a pasta: `cd vue-tasker`
3. Instale as dependências: `npm install`[cite: 1]

## Execução
Execute o servidor local com o comando:
`npm run dev`[cite: 1]
Acesse no navegador: `http://localhost:5173`[cite: 1]

## Estrutura do Projeto
* `src/App.vue`: Componente raiz (Root) que envolve a aplicação e contém a lógica da lista de tarefas[cite: 1].
* `src/main.js`: Ponto de entrada JS; instancia e monta o Vue na DOM[cite: 1].

## Funcionalidades
* Adicionar novas tarefas.
* Marcar tarefas como concluídas.
* Remover tarefas da lista.

## Vulnerabilidade Pesquisada
* **Identificador:** CVE-2024-6783[cite: 1]
* **Componente:** vue-template-compiler (Afeta projetos que ainda utilizam o Vue.js 2.x)[cite: 1]
* **Tipo:** Client-side Cross-Site Scripting (XSS) via Prototype Pollution[cite: 1]
* **Impacto:** Permite que um invasor injete e execute códigos JavaScript arbitrários no navegador do usuário[cite: 1].
* **Mitigação:** Migrar a aplicação para o Vue 3, que já possui essa falha corrigida nativamente[cite: 1].

## Evidências / Imagens
*(Tire um print da tela da sua aplicação rodando, arraste a imagem para cá e apague este aviso)*

## Link do GitHub Pages
Acesse a aplicação rodando aqui: `https://[SEU_USUARIO_DO_GITHUB].github.io/vue-tasker/`

## Referências
* https://vuejs.org/guide/scaling-up/sfc.html[cite: 1]
* https://vuejs.org/guide/extras/reactivity-in-depth.html[cite: 1]