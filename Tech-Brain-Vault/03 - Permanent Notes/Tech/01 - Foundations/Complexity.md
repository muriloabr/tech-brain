---
created: 2026-02-13 22:00
updated: 2026-02-18 02:53
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
aliases:
  - Complexidade Algorítmica
  - Time Complexity
  - Space Complexity
  - Big O
---

## Definição
**Complexity** (Complexidade) é a métrica usada para classificar a eficiência de um algoritmo, estimando como o consumo de recursos (Tempo de processamento e Espaço de memória) cresce à medida que o tamanho da entrada de dados (N) aumenta. Ela ignora hardware e velocidade exata em segundos, focando na taxa de crescimento da função.

## Funcionamento
A análise é geralmente expressa pela **Notação Big O** (O Grande-O), que descreve o "pior cenário" possível:
-   **O(1) - Constante:** O tempo é o mesmo, não importa se há 1 ou 1 milhão de itens (ex: acessar array pelo índice).
-   **O(n) - Linear:** O tempo dobra se os dados dobrarem (ex: percorrer uma lista).
-   **O(n²) - Quadrático:** O tempo quadruplica se os dados dobrarem (ex: loops aninhados).

## Comparação
| Foco da Análise | Time Complexity (Tempo) | Space Complexity (Espaço) |
| :--- | :--- | :--- |
| **Recurso** | Ciclos de CPU / Operações | Memória RAM / Stack |
| **Pergunta** | "Vai ficar lento com muitos dados?" | "Vai estourar a memória com muitos dados?" |
| **Trade-off** | Muitas vezes sacrificamos espaço (cache) para ganhar tempo. | Muitas vezes recalculamos (tempo) para economizar espaço. |