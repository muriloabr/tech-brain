---
created: 2026-02-13 22:13
updated: 2026-02-18 03:00
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Logic]]"
aliases:
  - Estruturas De Controle
  - Flow Control
  - Controle De Fluxo
---

## Definição
**Control Structures** (Estruturas de Controle) são blocos de programação que analisam variáveis e escolhem a direção que a execução do código deve seguir. Elas quebram a leitura linear (top-down) padrão do código, permitindo que o software tome decisões (pule partes), repita tarefas ou selecione caminhos diferentes baseados em condições lógicas.

## Funcionamento
O fluxo é ditado por três tipos fundamentais de estruturas:
1.  **Sequencial:** O padrão. Linha após linha.
2.  **Seleção (Decisão):** Usa a lógica booleana para bifurcar o caminho. Se *X* for verdade, faça *A*, senão, faça *B* (`if`, `else`, `switch`).
3.  **Repetição (Iteração):** Executa um bloco várias vezes enquanto uma condição for verdadeira (`for`, `while`), permitindo processar listas ou aguardar eventos.

## Comparação
| Característica | Execução Linear | Estrutura de Controle |
| :--- | :--- | :--- |
| **Caminho** | Único e previsível (Linha 1 -> 2 -> 3) | Ramificado e condicional |
| **Complexidade** | Baixa (apenas cálculos diretos) | Alta (lógica de negócios e regras) |
| **Analogia** | Ler um livro do início ao fim | Ler um livro de "Escolha sua Aventura" |