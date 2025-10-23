# Plataforma Web para ONGs - "Impacto Social"

Este é o projeto final da disciplina de Desenvolvimento Front-End, focado na criação de uma plataforma web completa e profissional para ONGs, utilizando HTML5, CSS3 e JavaScript avançado em uma arquitetura de Single Page Application (SPA).

## Visão Geral do Projeto

A plataforma "Impacto Social" é um sistema web que oferece a ONGs uma presença digital funcional para divulgar projetos, captar recursos e engajar voluntários. O sistema foi construído com foco em semântica, design responsivo, acessibilidade e interatividade.

## Tecnologias Utilizadas

* **HTML5:** Estruturação semântica do conteúdo.
* **CSS3:** Estilização, layout responsivo (Flexbox e Grid), Design System (Variáveis CSS).
* **JavaScript (ES6+ Modules):** Manipulação do DOM, interatividade, roteamento de cliente (SPA) e validação de formulários.

---

## Funcionalidades Implementadas

### Entrega 1: Estrutura (HTML)
* **Estrutura Semântica:** 3 páginas (Início, Projetos, Cadastro) estruturadas com tags semânticas (`<header>`, `<main>`, `<section>`, etc.).
* **Formulário Complexo:** Formulário de cadastro com validação nativa de HTML5, agrupamento (`<fieldset>`) e tipos de input modernos.
* **Máscaras de Input:** Implementação de JavaScript para máscaras de CPF, CEP e Telefone.

### Entrega 2: Estilização (CSS)
* **Design System:** Definição de paleta de cores, tipografia e espaçamentos via Variáveis CSS (`variables.css`).
* **Layout Responsivo:** Site 100% responsivo (Mobile-First) usando CSS Grid para layout principal e Flexbox para componentes.
* **Componentes:** Estilização de botões, cards, formulários e alertas.
* **Navegação:** Menu de navegação responsivo com menu hambúrguer em dispositivos móveis.
* **Validação Visual:** Formulários com feedback visual (bordas verdes/vermelhas) que só aparecem após a interação do usuário (`.interacted`).

### Entrega 3: Interatividade (JavaScript Avançado)
* **Single Page Application (SPA):** O site não recarrega mais a página. Um roteador JavaScript (`router.js`) intercepta os cliques, busca o conteúdo parcial da página (template) e o injeta dinamicamente no DOM.
* **Roteamento de Cliente:** Uso da History API (`pushState`, `popstate`) para atualizar a URL e permitir o uso dos botões de "Voltar" e "Avançar" do navegador.
* **Código Modular (ES6):** O JavaScript foi refatorado em módulos (`router.js`, `main.js`, `mascaras.js`) para organizar as funcionalidades e permitir a inicialização de scripts sob demanda.
* **Verificação de Consistência:** Sistema de validação de formulário que fornece feedback em tempo real (`blur`) e só permite o envio (`submit`) de dados válidos.

---

## Como Executar o Projeto

Como este projeto utiliza `fetch()` para carregar arquivos locais (`pages/*.html`) e Módulos ES6, ele **não funcionará** se você apenas abrir o `index.html` diretamente no navegador (devido à política de segurança CORS).

Para executar o projeto corretamente, você precisa de um servidor web local.

**A forma mais fácil é usando a extensão "Live Server" no VS Code:**
1.  Abra o projeto no Visual Studio Code.
2.  Instale a extensão `Live Server` (de Ritwick Dey).
3.  Clique com o botão direito no arquivo `index.html`.
4.  Selecione "Open with Live Server".

Isso iniciará um servidor local e abrirá o projeto no seu navegador.

---

## Estrutura de Pastas
Plataforma_ONG/

|

+-- index.html (A "casca" principal da SPA)

|

+-- pages/ (Os "templates" de conteúdo parcial)

| |

| +-- home.html

| +-- projetos.html

| +-- cadastro.html

|

+-- css/ (Todos os arquivos CSS modulares)

| |

| +-- base.css

| +-- components.css

| +-- layout.css

| +-- navigation.css

| +-- responsive.css

| +-- variables.css

|

+-- js/ (Todos os arquivos JavaScript modulares)

| |

| +-- main.js (Funções de UI: menu, formulário)

| +-- mascaras.js (Funções de máscara)

| +-- router.js (O cérebro da SPA)

|

+-- imagens/

| |

| +-- (logo, banners, fotos dos projetos...)

|

+-- README.md (Esta documentação)