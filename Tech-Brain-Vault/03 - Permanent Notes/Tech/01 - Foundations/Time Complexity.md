---
created: 2026-02-18 02:50
updated: 2026-02-18 02:51
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Complexity]]"
aliases:
  - Time Efficiency
  - Complexidade de Tempo
---

## Definição
A **Time Complexity** quantifica a quantidade de tempo computacional (número de operações elementares) que um algoritmo leva para executar como uma função do tamanho da entrada. É uma medida teórica de eficiência, focada na tendência de crescimento do esforço de processamento, não em segundos ou milissegundos.

## Funcionamento
A análise ocorre através da contagem de passos lógicos discretos — como atribuições, comparações e operações aritméticas — necessários para concluir a tarefa. O objetivo é determinar a relação entre o aumento dos dados de entrada ($n$) e o aumento das operações. Um algoritmo eficiente minimiza essa relação, permitindo o processamento de grandes volumes de dados sem degradação exponencial de performance.

## Comparação
Enquanto a **Space Complexity** se preocupa com o armazenamento de dados, a Time Complexity foca no ciclo de processamento da CPU. É possível (e comum) existir um *trade-off* entre ambos: técnicas como **Memoization** aumentam o uso de memória (Space) para reduzir drasticamente o número de recálculos necessários (Time).