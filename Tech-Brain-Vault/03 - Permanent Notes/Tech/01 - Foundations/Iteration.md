---
created: 2026-02-13 22:15
updated: 2026-02-18 02:55
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Control Structures]]"
aliases:
  - Iteração
  - Loops
  - Repetição
  - Laços
---

## Definição
**Iteration** (Iteração) é o processo computacional de repetir um bloco de instruções uma quantidade específica de vezes ou até que uma condição lógica seja satisfeita. É uma das formas primárias de controle de fluxo, permitindo que algoritmos processem coleções de dados (como listas) ou executem tarefas contínuas sem a necessidade de escrever o mesmo código repetidamente.

## Funcionamento
Um laço iterativo (loop) consiste em três partes:
1.  **Estado Inicial:** Onde o contador começa (ex: `i = 0`).
2.  **Condição de Parada:** A regra booleana testada antes de cada repetição. Se for falsa, o loop quebra.
3.  **Atualização:** A mudança no estado para avançar o processo (ex: `i++`), garantindo que o loop eventualmente termine.

## Comparação
| Característica | Iteração (Loops) | Recursão (Auto-chamada) |
| :--- | :--- | :--- |
| **Memória** | Eficiente e Constante (O(1)) | Consome Stack (O(N)) |
| **Estado** | Controlado por variáveis mutáveis (`i`) | Controlado por parâmetros de função |
| **Risco** | **Loop Infinito** (trava o programa) | **Stack Overflow** (trava + estoura memória) |
| **Uso Ideal** | Processar arrays, contadores simples | Navegar árvores, problemas matemáticos |
