---
created: 2026-02-13 22:10
updated: 2026-02-18 02:59
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Logic]]"
aliases:
  - Álgebra Booleana
  - Lógica Binária
  - Boolean Logic
---

## Definição
**Boolean Algebra** (Álgebra Booleana) é o ramo da matemática que lida com variáveis que têm apenas dois valores possíveis: Verdadeiro (`1`) ou Falso (`0`).  Diferente da álgebra elementar que usa números e operações aritméticas (+, -), a álgebra booleana usa valores lógicos e operações lógicas (E, OU, NÃO), servindo como a fundação matemática para todo o design de circuitos digitais e lógica de programação.

## Funcionamento
Ela opera manipulando estados binários através de operadores fundamentais:
-   **Conjunção (AND):** O resultado é 1 apenas se *ambas* as entradas forem 1 (A * B).
-   **Disjunção (OR):** O resultado é 1 se *pelo menos uma* entrada for 1 (A + B).
-   **Negação (NOT):** Inverte o valor. Se entra 1, sai 0 (¬A).
Essas operações são fisicamente implementadas em hardware através de transistores (Logic Gates).

## Comparação
| Conceito      | Álgebra Elementar              | Álgebra Booleana              |
| :------------ | :----------------------------- | :---------------------------- |
| **Valores**   | Infinitos (Reais, Inteiros...) | Binários (0 ou 1)             |
| **Operações** | Soma, Multiplicação, Divisão   | AND, OR, NOT, XOR             |
| **Aplicação** | Calcular quantidades e física  | Calcular decisões e circuitos |
| **Resultado** | Um número (`x = 42`)           | Um estado (`x = True`)        |