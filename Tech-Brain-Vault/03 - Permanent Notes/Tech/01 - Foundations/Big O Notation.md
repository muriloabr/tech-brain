---
created: 2026-02-18 02:34
updated: 2026-02-18 02:36
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Complexity]]"
aliases:
  - Notação Big O
  - Asymptotic Notation
  - Notação Grande-O
---

## Definição
A **Big O Notation** é a nomenclatura matemática padrão utilizada para classificar algoritmos de acordo com o crescimento de seus requisitos de tempo ou espaço à medida que o tamanho da entrada aumenta. Ela descreve o limite superior (pior caso) do comportamento de uma função, ignorando constantes e termos de ordem inferior para focar exclusivamente na taxa de crescimento.

## Funcionamento
O conceito opera simplificando a contagem exata de operações para uma ordem de magnitude. Ao analisar um algoritmo, identifica-se a operação dominante que se repete em função da entrada $n$.
Classes comuns de complexidade:
- **O(1)**: Constante. O tempo não muda, independente do tamanho da entrada.
- **O(log n)**: Logarítmica. O problema é dividido a cada passo (ex: Busca Binária).
- **O(n)**: Linear. O tempo cresce proporcionalmente à entrada.
- **O(n²)**: Quadrática. Típico de loops aninhados.

## Comparação
Diferente da medição de **Tempo de Execução** (wall-clock time), que varia conforme o hardware e a linguagem, a Big O é agnóstica à máquina. Enquanto o **Big Omega (Ω)** define o melhor caso (limite inferior) e o **Big Theta (Θ)** define o caso médio (limite estreito), a Big O é a métrica padrão da indústria por focar na escalabilidade sob estresse máximo.