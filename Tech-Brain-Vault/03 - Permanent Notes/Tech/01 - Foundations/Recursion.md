---
created: 2026-02-13 20:21
updated: 2026-02-18 03:04
type: concept
status: 🌳
area: Tech
tags: []
sources:
  - "[[Control Structures]]"
related:
  - Recursividade
  - Recursive Function
  - Função Recursiva
---

## Definição
**Recursion** (Recursão) é uma técnica de programação onde uma função resolve um problema chamando a si mesma com instâncias menores do problema original. É a base fundamental para algoritmos do paradigma **[[Divide and Conquer]]** e essencial para navegar estruturas não-lineares (como árvores).

## Funcionamento
Toda função recursiva bem formada deve possuir dois componentes obrigatórios:
1.  **[[Base Case]] (Caso Base):** A condição de parada. Quando atingida, a função retorna um valor simples sem fazer novas chamadas.
2.  **Passo Recursivo:** A parte onde a função chama a si mesma.
Cada chamada cria um novo frame na Call Stack. Isso significa que a recursão tem uma **[[Space Complexity]]** proporcional à profundidade da chamada (O(N)), diferente da iteração.

## Comparação
| Característica       | Recursão                                      | Iteração (Loops)                           |
| :------------------- | :-------------------------------------------- | :----------------------------------------- |
| **Custo de Memória** | **Alto**: Ocupa [[Space Complexity]] na Stack | **Baixo**: O(1) se não alocar dados extras |
| **Legibilidade**     | Alta para "Dividir e Conquistar"              | Alta para sequências lineares              |
| **Risco**            | **[[Stack Overflow]]**                        | [[Infinite Loop]]                          |
