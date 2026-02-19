---
created: 2026-02-13 22:03
updated: 2026-02-18 03:01
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Complexity]]"
aliases:
  - Estruturas De Dados
  - Containers
  - Collections
---

## Definição
**Data Structures** (Estruturas de Dados) são formatos especializados para organizar, processar, recuperar e armazenar dados na memória de um computador. A escolha da estrutura correta é determinante para a performance do software, pois cada uma oferece vantagens (trade-offs) específicas para operações de inserção, busca, ordenação ou deleção.

## Funcionamento
Elas operam definindo o layout dos dados na memória (Heap):
-   **Lineares:** Organizam dados sequencialmente (ex: Arrays, Linked Lists, Stacks, Queues). Fáceis de percorrer.
-   **Não-Lineares:** Organizam dados hierarquicamente ou por conexão (ex: Trees, Graphs). Melhores para relações complexas.
-   **Baseadas em Hash:** Mapeiam chaves para valores (ex: HashMaps, Dictionaries). Otimizadas para busca rápida.

## Comparação
| Estrutura            | Array (Vetor)                      | Linked List (Lista Ligada)             |
| :------------------- | :--------------------------------- | :------------------------------------- |
| **Memória**          | Bloco contíguo (vizinhos físicos)  | Nós dispersos apontando uns aos outros |
| **Acesso**           | Instantâneo O(1) via índice        | Lento O(n) (tem que percorrer tudo)    |
| **Inserção/Remoção** | Lenta (precisa deslocar elementos) | Rápida (só muda os ponteiros)          |
| **Tamanho**          | Fixo (geralmente)                  | Dinâmico                               |