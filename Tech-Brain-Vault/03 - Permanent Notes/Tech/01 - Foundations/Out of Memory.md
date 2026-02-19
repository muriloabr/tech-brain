---
created: 2026-02-13 20:57
updated: 2026-02-17 23:32
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Memory Leak]]"
aliases:
  - OOM
  - Memória Insuficiente
  - OOM Killer
---

## Definição
**Out of Memory** (OOM) é o estado crítico onde o sistema operacional ou a máquina virtual não possui mais memória [[RAM]] livre (física ou swap) para alocar a um processo. É o "ponto de ruptura" causado por vazamentos de memória ou dimensionamento incorreto de hardware.

## Funcionamento
Quando o **OOM** ocorre, o sistema toma medidas drásticas para sobreviver:
1.  **Rejeição:** Novas tentativas de alocação retornam erro ou exceção (`java.lang.OutOfMemoryError`).
2.  **Sacrifício (Linux):** O [[Kernel]] aciona o **OOM Killer**, um processo que analisa qual aplicação está consumindo mais memória (ou tem menor prioridade) e a encerra forçadamente (kill-9) para liberar recursos para o restante do sistema.

## Comparação
| Erro Fatal     | Out of Memory (Heap Space)            | Stack Overflow                      |
| :------------- | :------------------------------------ | :---------------------------------- |
| **Local**      | Memória Dinâmica (Heap)               | Memória de Execução (Stack)         |
| **Causa Raiz** | Muitos dados ou Vazamento (Leak)      | Recursão infinita ou muito profunda |
| **Velocidade** | Geralmente gradual (enche aos poucos) | Geralmente instantâneo              |
