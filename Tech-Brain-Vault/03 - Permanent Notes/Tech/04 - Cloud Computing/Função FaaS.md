---
created: 2026-02-09 17:22
updated: 2026-02-13 15:28
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Cold Start]]"
  - "[[Vendor Lock-in]]"
  - "[[BaaS]]"
  - "[[Microserviços]]"
aliases:
  - Serverless Function
  - Função Serverless
  - Functions em FaaS
---

## Definição
**Functions em FaaS (Function as a Service)** são unidades de código executadas sob demanda em plataformas serverless, nas quais o provedor de nuvem gerencia toda a infraestrutura necessária — servidores, runtime, escalabilidade e manutenção.  

A função é implantada como um artefato independente e acionada por eventos, executando apenas quando necessário.  

O desenvolvedor se concentra exclusivamente na lógica da função, enquanto o provedor cuida de toda a execução operacional.

Em [[FaaS]], funções **não ficam rodando continuamente**: elas são invocadas, executam sua tarefa e encerram, seguindo um modelo [[Event-Driven Architecture]].

## Funcionamento
Functions em FaaS operam por meio de um ciclo simples e completamente automatizado pelo provedor:
- **Evento:** Algo dispara a função (HTTP request, upload, fila, cron, webhook, trigger de banco, etc.).
- **Invocação:** A plataforma aloca automaticamente um ambiente de execução.
- **Execução:** A função processa a lógica definida pelo desenvolvedor.
- **Escalonamento:** Se múltiplos eventos chegam simultaneamente, a plataforma cria múltiplas instâncias automaticamente.
- **Finalização:** Após concluir, o ambiente é destruído ou hibernado, dependendo do provedor.

Características essenciais:
- **[[Stateless]]:** Cada invocação é isolada; nenhum estado persistente é mantido entre execuções.
- **Ephemeral:** O ambiente de execução dura apenas o tempo necessário.
- **Provisionamento automático:** O usuário nunca gerencia máquinas ou containers diretamente.
- **Cobrança por execução:** Pagamento baseado em invocações e tempo de CPU/memória consumido.

## Comparação
Comparativo entre **Functions em FaaS** e **Functions Genéricas (tradicionais)**.

| Característica      | Functions em FaaS (Serverless)                                                  | [[Função\|Function]] (Genéricas)                            |
| :------------------ | :------------------------------------------------------------------------------ | :---------------------------------------------------------- |
| **Execução**        | Sob demanda, acionada por eventos                                               | Chamadas diretamente pelo código                            |
| **Infraestrutura**  | Totalmente gerenciada pelo provedor                                             | Gerenciada pelo desenvolvedor ou pela aplicação             |
| **Estado**          | Stateless (cada invocação é isolada)                                            | Pode ser stateful ou stateless                              |
| **Escalabilidade**  | Automática, baseada em eventos                                                  | Limitada ao ambiente onde a aplicação está hospedada        |
| **Provisionamento** | Não existe para o usuário; a plataforma cria/destroi ambientes nos bastidores   | Necessita configurar servidores, containers, runtimes, etc. |
| **Modelo de Custo** | Pay-per-use (pago por invocações e tempo de execução)                           | Custo fixo da infraestrutura onde a aplicação roda          |
| **Uso**             | Cargas event-driven, pipelines, automações, APIs serverless                     | Lógica interna de aplicações, bibliotecas e sistemas locais |
| **Dependência**     | Depende de um serviço FaaS (AWS Lambda, Azure Functions, Cloud Functions, etc.) | Não depende de nuvem ou provedores                          |
