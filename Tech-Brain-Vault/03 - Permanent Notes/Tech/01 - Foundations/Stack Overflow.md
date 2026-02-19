---
created: 2026-02-13 20:27
updated: 2026-02-17 23:25
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
aliases:
  - Estouro De Pilha
  - Stack Exhaustion
---

## Definição
**Stack Overflow** é um erro de tempo de execução (Runtime Error) que ocorre quando um programa tenta usar mais espaço na [[Call Stack]] do que o sistema operacional alocou para ele. Como a [[Call Stack|Stack]] tem um tamanho fixo e limitado (geralmente entre 1MB e 8MB), exceder esse limite corrompe a memória adjacente, levando o SO a encerrar o processo imediatamente para proteção.

## Funcionamento
As causas técnicas principais são:
1.  **Recursão Infinita:** O caso mais comum. Uma função chama a si mesma sem atingir um Caso Base, empilhando frames infinitamente até o limite físico.
2.  **Recursão Muito Profunda:** O algoritmo está correto, mas o volume de dados exige mais passos do que a pilha suporta (ex: percorrer uma lista ligada de 1 milhão de itens recursivamente).
3.  **Alocação Excessiva na Stack:** Declarar variáveis locais gigantescas (como arrays ou matrizes enormes) dentro de uma função, em vez de usar a Heap.

## Comparação
| Tipo de Erro     | Stack Overflow                                 | Out of Memory (Heap)                           |
| :--------------- | :--------------------------------------------- | :--------------------------------------------- |
| **Origem**       | Esgotamento da Pilha de Execução               | Esgotamento da RAM disponível (Heap)           |
| **Causa Típica** | Lógica (recursão ruim) ou Arquitetura          | Vazamento de memória ou Carga de dados massiva |
| **Sintoma**      | Crash imediato e abrupto ("Segfault")          | Lentidão progressiva (Swap) seguida de Crash   |
| **Resolução**    | Corrigir a condição de parada ou usar iteração | Otimizar uso de objetos ou aumentar RAM        |