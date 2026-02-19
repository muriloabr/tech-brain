---
created: 2026-02-18 02:35
updated: 2026-02-18 02:37
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
aliases:
  - Condição de Parada
  - Halting Condition
  - Caso Base
---

## Definição
O **Base Case** é a condição fundamental em um algoritmo recursivo que permite que a função retorne um valor sem realizar novas chamadas a si mesma. Ele atua como a âncora lógica que interrompe a cadeia de recursão, prevenindo a execução infinita.

## Funcionamento
Em qualquer função recursiva, a lógica verifica primeiramente se o estado atual satisfaz a condição de parada.
- Se **Sim**: O algoritmo retorna um resultado concreto (valor fixo) e começa a desempilhar a memória (**Call Stack**).
- Se **Não**: O algoritmo continua para o Passo Recursivo, modificando a entrada em direção ao caso base.
Sem um caso base atingível, o programa consome toda a memória disponível, resultando em um erro de *Stack Overflow*.

## Comparação
O Base Case é o oposto funcional do **Recursive Step**. Enquanto o passo recursivo expande o problema e aprofunda a pilha de execução, o caso base contrai o problema e inicia o retorno dos dados. Em loops iterativos (como `while`), seu equivalente é a condição de saída (ex: `i < 10`).