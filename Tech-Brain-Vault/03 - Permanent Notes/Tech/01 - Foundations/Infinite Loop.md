---
created: 2026-02-18 03:03
updated: 2026-02-18 03:07
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related: []
aliases:
  - Loop Infinito
  - Endless Loop
  - Ciclo Infinito
---

## Definição
Um **Infinite Loop** é uma sequência de instruções em um programa de computador que se repete indefinidamente, pois a condição de término necessária para encerrar a execução nunca é satisfeita.

Na maioria dos contextos de desenvolvimento, é considerado um erro lógico crítico (bug), resultando no travamento da aplicação ou no consumo excessivo de recursos da CPU, embora seja utilizado intencionalmente em arquiteturas específicas como **Event Listeners** ou servidores.

## Funcionamento
O ciclo ocorre quando o fluxo de controle é direcionado repetidamente para o início do bloco de código sem que haja uma mudança de estado capaz de validar a condição de saída.
Causas técnicas comuns:
1.  **Condição Estática**: A expressão de controle é permanentemente avaliada como `true` (ex: `while(true)`).
2.  **Ausência de Iteração**: A variável de controle (contador) não é incrementada ou modificada dentro do corpo do loop.
3.  **Lógica Divergente**: A atualização da variável afasta o valor da condição de parada em vez de aproximá-lo.
Em sistemas operacionais, um loop infinito não intencional pode acionar mecanismos de segurança, como o *Watchdog Timer*, para forçar o encerramento do processo.

## Comparação
A distinção fundamental entre um loop infinito e outros erros de repetição reside no recurso esgotado.

| Característica | Infinite Loop                                               | Infinite Recursion                                      | Deadlock                                                     |
| :------------- | :---------------------------------------------------------- | :------------------------------------------------------ | :----------------------------------------------------------- |
| **Mecanismo**  | Repetição iterativa (instrução `JUMP`).                     | Chamadas de função aninhadas.                           | Bloqueio mútuo de recursos.                                  |
| **Sintoma**    | Alto uso de CPU (100% em um núcleo), interface congelada.   | Erro de **Stack Overflow** (estouro de pilha).          | Uso de CPU zero (processo em estado de espera), mas travado. |
| **Memória**    | Geralmente constante (não aloca nova memória a cada ciclo). | Crescimento exponencial da memória Stack até o colapso. | Constante.                                                   |
| **Resolução**  | Interrupção forçada do processo (Kill).                     | Correção do Base Case.                                  | Reinício ou preempção de recursos.                           |
