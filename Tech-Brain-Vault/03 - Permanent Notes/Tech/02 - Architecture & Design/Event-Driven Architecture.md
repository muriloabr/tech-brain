---
created: 2026-02-08 20:17
updated: 2026-02-13 15:29
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Asynchronous Processing]]"
  - "[[Serverless Computing]]"
  - "[[Microserviços]]"
  - "[[Decoupling]]"
aliases:
  - EDA
  - Arquitetura Orientada a Eventos
---

## Definição
**Event-Driven Architecture (EDA)** é um padrão de [[Arquitetura de Software]] onde o fluxo de execução e a comunicação entre serviços são determinados pela ocorrência de eventos (mudanças de estado), em vez de chamadas diretas e sequenciais. Neste modelo, os componentes são altamente desacoplados: quem gera o evento (Produtor) não precisa conhecer quem vai processá-lo (Consumidor), nem se ele foi processado com sucesso imediato.

## Funcionamento
O fluxo da EDA baseia-se em três componentes principais interagindo de forma assíncrona:
- **Produtor (Producer):** Detecta ou gera um evento (ex: "Pedido Criado", "Sensor Ativado") e o envia para um roteador. 
- **Roteador/Broker ([[Barramento de Eventos]]):** O intermediário (ex: [[Kafka]], [[RabbitMQ]], [[AWS EventBridge]]) que recebe o evento, filtra e o distribui para os interessados. 
- **Consumidor (Consumer):** O serviço (ou [[Função FaaS]]) que assina aquele tipo de evento e reage a ele (ex: "Enviar Email de Confirmação").

### Variações no Contexto Serverless
Embora o [[Serverless Computing]] seja inerentemente acionado por eventos, a arquitetura pode assumir duas formas: 

| Modelo | Comportamento | Exemplo Típico |
| :--- | :--- | :--- |
| **Pub/Sub (Publish-Subscribe)** | Um evento é enviado e *múltiplos* consumidores reagem simultaneamente. | Upload de foto -> (Função 1: Gera Thumb) + (Função 2: Atualiza DB). |
| **Streaming de Eventos** | Fluxo contínuo de dados processados em tempo real. | Cliques no site -> Análise de fraude em tempo real. |
| **Filas (Queues)** | Eventos são empilhados para processamento sequencial (buffer). | Picos de Black Friday -> Processar pedidos um por um sem derrubar o banco. |

## Comparação
Comparando o tradicional [[Request-Driven]] com Event-Driven:

| Característica     | [[Request-Driven]](Tradicional/REST)        | Event-Driven(EDA)                              |     |
| :----------------- | :------------------------------------------ | :--------------------------------------------- | --- |
| **Acoplamento**    | Alto (A conhece B e espera B).              | Baixo (A não conhece B).                       |     |
| **Comunicação**    | Síncrona (Bloqueante).                      | Assíncrona (Não-bloqueante).                   |     |
| **Escalabilidade** | Limitada pelo serviço mais lento da cadeia. | Independente para cada consumidor.             |     |
| **Complexidade**   | Menor (fluxo linear fácil de rastrear).     | Maior (necessita observabilidade distribuída). |     |
|                    |                                             |                                                |     |
