---
created: 2026-02-17 23:36
updated: 2026-02-18 03:09
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
aliases:
  - Gerenciamento de Memória
  - Gestão de Memória
---

## Definição
O **Memory Management** é o subsistema crítico responsável pela alocação, monitoramento e liberação da memória principal (RAM) de um computador. Ele atua como uma interface entre o hardware e os processos de software, garantindo que cada aplicativo tenha acesso ao espaço necessário para execução sem interferir na estabilidade do sistema ou nos dados de outros programas. Sua função primordial é maximizar a eficiência do uso da memória disponível enquanto implementa mecanismos de proteção e isolamento.

## Funcionamento
O processo opera através da abstração do endereçamento físico em endereçamento lógico, utilizando unidades de hardware como a **MMU (Memory Management Unit)**. O ciclo de vida compreende três etapas fundamentais: alocação (reserva de espaço), utilização (leitura/escrita) e reciclagem (liberação para reuso).

Para gerenciar recursos limitados, o sistema emprega técnicas avançadas:
1. **Tradução de Endereços**: Mapeia endereços virtuais gerados pela CPU para endereços físicos na RAM.
2. **Paginação e Segmentação**: Divide a memória em blocos fixos (páginas) ou variáveis (segmentos) para evitar fragmentação e facilitar a troca de dados com o armazenamento secundário.
3. **Swapping**: Move dados inativos da RAM para o disco (espaço de troca) quando a memória principal está cheia, expandindo a capacidade aparente através de [[Virtual Memory]].

Em linguagens de programação, o gerenciamento ocorre em duas áreas distintas:
- **Stack**: Alocação estática e ordenada para variáveis locais e chamadas de função (LIFO).
- **Heap**: Alocação dinâmica e desordenada para objetos que precisam persistir além do escopo imediato.

## Comparação
A principal distinção na implementação do gerenciamento de memória ocorre na responsabilidade pela desalocação de recursos.

| Característica | Gerenciamento Manual                                           | Gerenciamento Automático                                      |
| :------------- | :------------------------------------------------------------- | :------------------------------------------------------------ |
| **Controle**   | Total e explícito pelo programador.                            | Delegado ao ambiente de execução (Runtime).                   |
| **Mecanismo**  | Uso de comandos diretos (ex: `malloc`/`free` em **C**).        | Uso de **Garbage Collection** (ex: **Java**, **Python**).     |
| **Desempenho** | Previsível e otimizado, sem pausas inesperadas.                | Pode sofrer latência devido aos ciclos de limpeza do coletor. |
| **Riscos**     | Alto risco de vazamento de memória (Memory Leaks) e corrupção. | Maior consumo de recursos computacionais (overhead).          |
| **Uso Típico** | Sistemas embarcados, drivers, jogos AAA.                       | Aplicações web, scripts, softwares corporativos.              |