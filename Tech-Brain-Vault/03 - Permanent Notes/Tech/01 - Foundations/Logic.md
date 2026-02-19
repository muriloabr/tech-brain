---
created: 2026-02-13 21:37
updated: 2026-02-18 03:00
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Boolean Algebra]]"
aliases:
  - Lógica Booleana
  - Lógica Computacional
  - Formal Logic
---

## Definição
**Logic** (Lógica) na ciência da computação é a base matemática que permite a tomada de decisões e o controle de fluxo em algoritmos. Baseada fundamentalmente na Álgebra Booleana, ela lida com valores de verdade (`True`/`False`) e operadores que combinam essas verdades para criar condições complexas, permitindo que o software reaja a diferentes cenários.

## Funcionamento
Os computadores operam através de portas lógicas (físicas) que são abstraídas em operadores lógicos (software):
-   **AND (E):** Verdadeiro apenas se *todas* as condições forem verdadeiras.
-   **OR (OU):** Verdadeiro se *pelo menos uma* condição for verdadeira.
-   **NOT (NÃO):** Inverte o valor (Verdadeiro vira Falso).
-   **XOR (Ou Exclusivo):** Verdadeiro apenas se as condições forem diferentes entre si.

## Comparação
| Conceito | Lógica Proposicional | Controle de Fluxo (Flow Control) |
| :--- | :--- | :--- |
| **Natureza** | Teórica/Matemática | Prática/Implementação |
| **Exemplo** | `P AND Q -> R` | `if (user && password) { login() }` |
| **Objetivo** | Provar validade | Executar caminhos diferentes |