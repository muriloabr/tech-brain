---
created: 2026-02-08 19:48
updated: 2026-02-13 15:29
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Microserviços]]"
  - "[[Cloud Infrastructure]]"
aliases:
  - Functions as a Service
  - Função como Serviço
  - Função
  - Functions
---

## Definição
**FaaS (Function as a Service)** é um modelo de computação em nuvem que permite aos desenvolvedores executar trechos de código ([[Função FaaS]]) em resposta a eventos específicos, sem a necessidade de gerenciar a infraestrutura subjacente. É a unidade mais granular da [[Arquitetura Serverless]], onde o foco recai inteiramente na lógica de execução efêmera(curtíssima duração, passageiro, transitório ou temporário).

## Funcionamento
O ciclo de vida de uma **FaaS** é baseado em gatilhos ([[Event Trigger]]). Quando um evento ocorre (como um upload de arquivo, uma [[Requisição HTTP]] ou uma alteração no banco de dados), o provedor de nuvem instancia um container temporário, executa a função e o encerra imediatamente após a conclusão.

**Principais características:**
- **Escalabilidade Automática:** O provedor escala as funções horizontalmente de forma instantânea.    
- **Cobrança Granular:** Paga-se apenas pelo tempo de execução (geralmente medido em milissegundos) e memória consumida.    
- **Efemeridade:** As funções são [[Stateless]](sem estado); qualquer dado que precise ser persistido deve ser enviado para um banco de dados ou storage externo.

## Comparação

| **Característica** | **FaaS (Function as a Service)**                 | **PaaS (Platform as a Service)**                                      |
| ------------------ | ------------------------------------------------ | --------------------------------------------------------------------- |
| **Escalabilidade** | Automática e altamente granular (por invocação). | Geralmente baseada em instâncias ou instâncias de container.          |
| **Abstração**      | O desenvolvedor gere apenas a função/lógica.     | O desenvolvedor gere a aplicação completa e configurações de runtime. |
| **Custo**          | [[Pay-per-use]] (milissegundos de execução).     | Geralmente [[Pay-per-hour]] ou por recursos reservados.               |
| **Estado**         | Estritamente [[Stateless]].                      | Pode ser [[Stateful]] ou [[Stateless]].                               |
