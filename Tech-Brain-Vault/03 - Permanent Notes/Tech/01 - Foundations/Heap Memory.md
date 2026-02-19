---
created: 2026-02-13 20:12
updated: 2026-02-17 23:33
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
aliases:
  - Heap
  - Memória Dinâmica
  - Dynamic Memory
---

## Definição
**Heap Memory** (Memória Heap) é uma região de memória grande e não estruturada usada para alocação dinâmica. Diferente da [[Call Stack|Stack]], que é automática e linear, a **Heap** permite que o programador (ou o runtime da linguagem) solicite blocos de memória de tamanho arbitrário a qualquer momento, que persistem até serem explicitamente liberados ou coletados pelo Garbage Collector.

## Funcionamento
O gerenciamento ocorre via ponteiros e alocadores de memória:
1.  **Alocação:** O programa solicita espaço (ex: `malloc` em C, `new` em Java). O sistema operacional busca um bloco livre adequado na "pilha de desordem" e retorna o endereço dele.
2.  **Acesso:** O acesso é indireto e ligeiramente mais lento, pois a [[CPU]] precisa ler o ponteiro na Stack para encontrar o dado na Heap.
3.  **Fragmentação:** Com o tempo, alocações e desalocações criam "buracos" na memória, exigindo desfragmentação ou compactação.
4.  **Liberação:** Em linguagens manuais (C/C++), o desenvolvedor deve liberar a memória (`free`). Em linguagens gerenciadas (Java, C#, Python), o Garbage Collector rastreia e limpa objetos órfãos.

## Comparação
| Aspecto             | Heap Memory                                           | [[Call Stack\|Stack Memory]]              |
| :------------------ | :---------------------------------------------------- | :---------------------------------------- |
| **Visibilidade**    | Global (acessível por qualquer função com o ponteiro) | Local (restrita ao escopo da função)      |
| **Flexibilidade**   | Alta (redimensionável, tempo de vida indefinido)      | Baixa (tamanho fixo, tempo de vida curto) |
| **Custo de Gestão** | Alto (complexidade de alocação/liberação)             | Zero (instrução simples de push/pop)      |
| **Problema Comum**  | Memory Leak (Vazamento)                               | Stack Overflow (Estouro)                  |