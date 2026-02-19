---
created: 2026-02-18 02:28
updated: 2026-02-18 02:53
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Complexity]]"
aliases:
  - Space Efficiency
  - Complexidade de Espaço
---

## Definição
A **Space Complexity** mede a quantidade total de memória de trabalho (RAM) que um algoritmo necessita para executar até sua conclusão, em função do tamanho da entrada. Ela engloba tanto o espaço fixo (código, constantes) quanto o espaço variável (alocações dinâmicas, pilhas de recursão).

## Funcionamento
O cálculo considera dois componentes principais:
1.  **Espaço Auxiliar**: A memória extra usada temporariamente pelo algoritmo (variáveis de controle, estruturas de dados provisórias).
2.  **Espaço de Entrada**: A memória necessária para armazenar os dados originais.
Em análises modernas, foca-se frequentemente no espaço auxiliar para determinar se o algoritmo opera *in-place* (sem memória extra significativa) ou se requer estruturas duplicadas.

## Comparação
Diferente da **Time Complexity**, onde o objetivo é sempre a velocidade máxima, a otimização de espaço lida com um limite físico rígido (a quantidade de RAM disponível). Um algoritmo que excede a memória disponível falhará (Crash ou **Out of Memory**), enquanto um algoritmo lento apenas demorará a concluir.