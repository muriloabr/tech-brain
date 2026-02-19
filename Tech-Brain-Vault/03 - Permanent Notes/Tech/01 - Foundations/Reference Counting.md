---
created: 2026-02-13 21:06
updated: 2026-02-17 23:24
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Heap Memory]]"
aliases:
  - RefCount
  - Contagem de Referência
---

## Definição
**Reference Counting** (Contagem de Referência) é uma técnica simples de gerenciamento de memória onde cada objeto armazena um contador numérico de quantas referências (ponteiros) apontam para ele. Quando esse contador chega a zero — ou seja, ninguém mais "conhece" o objeto — ele é considerado lixo e sua memória é imediatamente liberada.

## Funcionamento
O mecanismo é determinístico e ocorre em tempo real:
1.  **Incremento:** Toda vez que uma variável é atribuída a um objeto (ex: `a = objeto`), o contador do objeto sobe (+1).
2.  **Decremento:** Quando a variável sai de escopo ou muda de valor (ex: `a = null`), o contador desce (-1).
3.  **Liberação:** Se o contador atingir 0, o destrutor do objeto é chamado e a memória volta para a Heap.

## Comparação
| Característica | Reference Counting | Mark-and-Sweep (GC Tracing) |
| :--- | :--- | :--- |
| **Velocidade** | Distribui o custo ao longo da execução | Gera pausas ("Stop the world") para limpar |
| **Problema Crítico** | **Referência Circular** (A aponta B, B aponta A) causa Leak | Resolve referências circulares nativamente |
| **Uso** | Python, PHP, Swift (ARC), C++ (Smart Pointers) | Java, C#, Go, JavaScript (V8) |