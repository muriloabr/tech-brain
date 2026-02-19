---
created: 2026-02-13 20:53
updated: 2026-02-17 23:32
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related: []
aliases:
  - Vazamento de Memória
  - Memory Bloat
---

## Definição
**Memory Leak** (Vazamento de Memória) é um defeito de software onde o programa aloca memória (geralmente na [[Heap Memory|Heap]]) mas falha em liberá-la após o uso. Como consequência, esses blocos de memória permanecem ocupados e indisponíveis para outros processos, acumulando-se ao longo do tempo até esgotar os recursos do sistema.

## Funcionamento
Ocorre quando a referência a um objeto é perdida, mas o objeto não é destruído:
1.  **Em linguagens manuais (C):** O programador faz `malloc` mas esquece do `free`.
2.  **Em linguagens gerenciadas (Java/JS):** O programador mantém acidentalmente uma referência ativa a um objeto inútil (ex: um listener esquecido em um botão removido da tela), impedindo o Garbage Collector de limpar.

## Comparação
| Cenário           | Memory Leak                         | Uso Alto de Memória (High Usage)  |
| :---------------- | :---------------------------------- | :-------------------------------- |
| **Comportamento** | Crescimento contínuo e irreversível | Sobe e desce conforme a carga     |
| **Causa**         | Bug / Código defeituoso             | Necessidade legítima da aplicação |
| **Resultado**     | Crash eventual (Out of Memory)      | Lentidão (Swap), mas recupera     |
