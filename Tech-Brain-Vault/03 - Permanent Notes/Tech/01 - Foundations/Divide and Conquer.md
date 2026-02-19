---
created: 2026-02-18 02:38
updated: 2026-02-18 02:41
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Algorithm Paradigms]]"
aliases:
  - Divisão e Conquista
  - Divide & Conquer
---

## Definição
**Divide and Conquer** é um paradigma algorítmico que resolve problemas complexos quebrando-os recursivamente em dois ou mais subproblemas do mesmo tipo ou relacionados, até que estes se tornem simples o suficiente para serem resolvidos diretamente.

## Funcionamento
A estratégia segue rigorosamente três etapas:
1.  **Dividir**: O problema original é particionado em subproblemas menores.
2.  **Conquistar**: Os subproblemas são resolvidos recursivamente. Se forem pequenos o suficiente (atingirem o **Base Case**), são resolvidos trivialmente.
3.  **Combinar**: As soluções dos subproblemas são mescladas para formar a solução do problema original.
Exemplos clássicos incluem Merge Sort, Quick Sort e Busca Binária.

## Comparação
Diferente da **Dynamic Programming**, que é usada quando os subproblemas se sobrepõem e se repetem, o Divide and Conquer é ideal quando os subproblemas são independentes e disjuntos. Enquanto **Greedy** toma decisões lineares sem olhar para trás, este paradigma trabalha na ramificação e recomposição da estrutura de dados.