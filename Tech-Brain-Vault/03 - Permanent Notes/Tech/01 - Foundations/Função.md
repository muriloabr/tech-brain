---
created: 2026-02-09 17:22
updated: 2026-02-13 15:29
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Modular Programming]]"
  - "[[Clean Code]]"
  - "[[Algoritmos]]"
  - "[[Call Stack]]"
aliases:
  - Function
  - Subrotina
  - Routine
---

## Definição
No contexto de [[Ciência da Computação]] e [[Arquitetura de Software]], uma **Function** (Função) é um bloco de código autônomo e encapsulado, projetado para realizar uma tarefa única e específica. Ela atua como a unidade fundamental da lógica de programação, permitindo a reutilização de código e a modularidade.

Matematicamente, mapeia entradas (argumentos/parâmetros) para saídas (retornos), embora em programação possa realizar "efeitos colaterais" (alterar estados fora de seu escopo local). 

É o conceito base que, quando escalado para [[Infraestrutura em Nuvem]], dá origem ao [[FaaS]], mas fundamentalmente é uma estrutura lógica de organização de instruções.

## Funcionamento
O ciclo de vida de uma função opera, em termos gerais, através da manipulação da **Pilha de Execução ([[Call Stack]])**:
- **Declaração/Definição:** O desenvolvedor define a assinatura (nome, parâmetros esperados e tipo de retorno) e o corpo (a lógica interna).
- **Invocação (Chamada):** Quando o programa principal ou outra função "chama" esta função, o fluxo de execução é desviado.
- **Contexto de Execução:** Um novo quadro (frame) é empilhado na memória. Variáveis locais são criadas e existem apenas dentro deste contexto.
- **Processamento:** As instruções são executadas sequencialmente.
- **Retorno e Desalocação:** Ao finalizar ou encontrar um comando `return`, o valor é passado de volta ao chamador, o quadro é removido da pilha e a memória local é liberada.

### Características Principais
* **Modularidade:** Divide problemas complexos em partes menores e gerenciáveis.
* **Abstração:** O usuário da função não precisa saber *como* ela faz, apenas *o que* ela faz (caixa preta).
* **Escopo:** Isolamento de variáveis para evitar conflitos de nomes (poluição do escopo global).

## Comparação
Abaixo, a distinção entre a **Função** como unidade lógica de código, o [[FaaS]] (sua implementação em nuvem) e um [[Método]] (sua implementação em Orientação a Objetos).

| Característica     | Function (Conceito Puro)                            | [[FaaS]] (Function-as-a-Service)                                                                                        | Método (Method)                           |
| :----------------- | :-------------------------------------------------- | :---------------------------------------------------------------------------------------------------------------------- | :---------------------------------------- |
| **Natureza**       | Unidade Lógica de Código                            | Unidade de Implantação (Cloud)                                                                                          | Comportamento de Objeto                   |
| **Estado**         | Pode ou não ter estado ([[Stateful]]/[[Stateless]]) | Geralmente Stateless (sem estado persistente local)                                                                     | Vinculado ao estado do Objeto (this/self) |
| **Acionamento**    | Chamada explícita no código                         | Eventos (HTTP, Filas, Cron, Uploads)                                                                                    | Chamada via instância de classe           |
| **Infraestrutura** | Processo da aplicação local                         | Gerenciada pelo provedor Cloud                                                                                          | Processo da aplicação local               |
| **Latência**       | Nanossegundos/Microssegundos                        | Milissegundos (pode sofrer Cold Start)                                                                                  | Nanossegundos/Microssegundos              |
| **Dependência**    | Compilador/Interpretador da linguagem               | Plataforma do Cloud Provider ([[Amazon Web Services\|AWS]], [[Microsoft Azure\|Azure]], [[Google Cloud Platform\|GCP]]) | Classe/Instância                          |
