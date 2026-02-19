---
created: 2026-02-09 17:15
updated: 2026-02-13 15:33
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[RabbitMQ]]"
  - "[[Asynchronous Communication]]"
  - "[[Kafka]]"
aliases:
  - Event Bus / Queue
  - Fila de Mensagens
  - Message Queue
---

## Definição
**Event Bus** (Barramento) e **Message Queue** (Fila) são mecanismos de infraestrutura que permitem a comunicação assíncrona entre diferentes partes de um sistema, agindo como intermediários que recebem, armazenam e entregam mensagens.

Eles desacoplam o produtor da informação do consumidor da informação.

## Funcionamento
Embora parecidos, têm propósitos distintos:
- **Queue (Fila - Point-to-Point):** Um produtor envia uma mensagem e *apenas um* consumidor a processa. Útil para distribuir carga de trabalho (ex: processar pagamentos).
- **Bus/Topic (Pub/Sub):** Um produtor publica um evento e *todos* os assinantes interessados recebem uma cópia. Útil para notificar mudanças de estado (ex: "Cliente Criado" -> avisa Email, avisa Logística, avisa CRM).

## Comparação
Síncrono (Direto) vs. Assíncrono (Bus/Queue)

| Critério | Comunicação Síncrona (REST) | Comunicação Assíncrona (Queue/Bus) |
| :--- | :--- | :--- |
| **Dependência Temporal** | Alta (Ambos devem estar online agora). | Baixa (Consumidor pode processar depois). |
| **Bloqueio** | O remetente espera a resposta. | O remetente "dispara e esquece" (Fire & Forget). |
| **Tratamento de Picos** | Sistema pode cair por sobrecarga. | A fila age como amortecedor (Buffer). |
| **Acoplamento** | Conhece o endereço do destino. | Conhece apenas a fila/tópico. |