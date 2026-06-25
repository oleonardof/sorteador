# Sortify — Raffle Engine v2.0

Um sorteador moderno e futurista para nomes e números, construído com foco em performance, design de interface (UI) e experiência do usuário (UX). O sistema garante que não haja repetições nos sorteios utilizando um pool dinâmico de itens.

## 🚀 Recursos

* **Sem Repetição (Pool Dinâmico):** Os itens sorteados são removidos da lista principal automaticamente, garantindo que ninguém ou nenhum número seja sorteado duas vezes.
* **Dois Modos de Operação:**
  * **Nomes:** Cole uma lista de participantes. Permite ordenação alfabética ou por ordem de sorteio.
  * **Números:** Defina um intervalo (ex: 1 a 100). Suporta diferentes formatos de saída (Simples, Com zeros `001`, ou Hexadecimal).
* **Altamente Customizável:** Defina a quantidade de itens a serem sorteados de uma vez e ajuste a velocidade da animação do sorteio.
* **Histórico Detalhado:** Acompanhe todos os sorteios realizados na sessão, divididos por rodadas (ex: 1º Sorteio, 2º Sorteio).
* **Estatísticas em Tempo Real:** Monitore o total de itens, quantos já foram sorteados e quantos restam no pool.
* **Exportação Rápida:** Botão integrado para copiar o resultado exato para a área de transferência com feedback visual (Toast).
* **Animações e Efeitos Visuais:** Efeitos de partículas em canvas, *glitch* nos resultados, barra de progresso e paleta de cores *dark mode* inspirada em ficção científica.

## 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido de forma "Vanilla", sem a necessidade de frameworks ou bibliotecas externas pesadas, garantindo carregamento instantâneo.

* **HTML5:** Semântica e estrutura.
* **CSS3:** Variáveis customizadas (CSS Variables), Flexbox, CSS Grid, animações (`@keyframes`), backdrop-filter e design responsivo.
* **JavaScript (ES6+):** Manipulação do DOM, lógica de manipulação de arrays (pool de sorteio), temporizadores para animação e API de Clipboard.
* **Google Fonts:** Orbitron (títulos e números), Share Tech Mono (dados técnicos) e Inter (textos gerais).

## 📦 Como Usar

Não é necessário nenhum processo de instalação ou build.

1. Faça o clone deste repositório ou baixe o arquivo fonte.
2. Dê um clique duplo no arquivo `index.html` para abri-lo em qualquer navegador web moderno (Chrome, Firefox, Edge, Safari).
3. Na tela inicial, clique em **⚡ Iniciar Sorteio**.
4. Escolha entre a aba **Nomes** ou **Números**.
5. Configure a lista ou o intervalo desejado e clique em **⚡ Sortear**.

## ⚙️ Estrutura do Código

Toda a aplicação está contida em um único arquivo (Single-File Component style) para máxima portabilidade:

* `<style>`: Contém toda a estilização, separada por componentes (Background, Buttons, Tabs, Display, Histórico).
* `<div id="bg">` e `<canvas id="particles">`: Responsáveis pelo fundo e animação das partículas em movimento.
* `<script>`: Contém a lógica dividida em:
  * Sistema de partículas (Canvas API).
  * Navegação entre Home e App.
  * Gerenciamento de estado (Tabs, Pool de Nomes, Pool de Números).
  * Lógica de Sorteio e Animação (`setInterval`).
  * Atualização de Histórico e Estatísticas.
