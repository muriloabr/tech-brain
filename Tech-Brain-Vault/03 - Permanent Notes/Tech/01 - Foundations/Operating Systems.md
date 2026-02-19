---
created: 2026-02-18 03:06
updated: 2026-02-18 03:08
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related: []
aliases:
  - Sistemas Operacionais
  - OS
  - SO
---

## Definição
O **Operating System** (OS) é o software de sistema fundamental que atua como intermediário entre o hardware do computador e as aplicações do usuário. Ele gerencia, abstrai e orquestra os recursos físicos (processador, memória, disco, periféricos), fornecendo uma interface padronizada (API) para que programas possam ser executados sem precisar manipular diretamente os complexos componentes eletrônicos.

## Funcionamento
A operação central baseia-se no **Kernel** (núcleo), a primeira parte do sistema carregada na memória durante o boot. O OS funciona através de um ciclo contínuo de interrupções e chamadas de sistema (**System Calls**):
1.  **Abstração**: Converte comandos complexos de hardware em funções simples de software (ex: "gravar arquivo" em vez de "mover cabeça de leitura do disco para setor X").
2.  **Gerenciamento de Recursos**: Utiliza algoritmos de escalonamento para decidir qual processo usa a CPU ([[Process Management]]) e como a RAM é distribuída ([[Memory Management]]).
3.  **Proteção**: Opera em dois modos distintos — **User Mode** (restrito, para apps) e **Kernel Mode** (irrestrito, para o núcleo) — prevenindo que um erro em um programa derrube todo o sistema.

## Comparação
A distinção crítica na arquitetura de sistemas operacionais reside na finalidade do escalonamento de tarefas.

| Característica    | GPOS (General Purpose OS)                                   | RTOS (Real-Time OS)                                           |
| :---------------- | :---------------------------------------------------------- | :------------------------------------------------------------ |
| **Exemplos**      | **Windows**, **Linux**, **macOS**.                          | **VxWorks**, **FreeRTOS**, Sistemas de Aviônica.              |
| **Objetivo**      | Maximizar o throughput (vazão) e a conveniência do usuário. | Garantir o determinismo e o cumprimento de prazos rígidos.    |
| **Latência**      | Variável; atrasos são toleráveis (ex: abrir um vídeo).      | Previsível; atrasos são falhas críticas (ex: acionar airbag). |
| **Escalonamento** | Baseado em justiça (fairness) e prioridade dinâmica.        | Baseado em prioridade fixa e preempção imediata.              |