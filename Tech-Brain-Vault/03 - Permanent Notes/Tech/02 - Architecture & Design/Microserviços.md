---
created: 2026-02-09 16:49
updated: 2026-02-13 15:29
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Containerization]]"
  - "[[DevOps]]"
  - "[[Service Mesh]]"
aliases:
  - Microservices
  - Microserviço
  - Microservice
  - Arquitetura de Microserviços
  - Microservices Architecture
---

## Definição
**Microservices Architecture** é uma abordagem arquitetural onde uma aplicação é estruturada como uma coleção de serviços pequenos, autônomos e fracamente acoplados, modelados ao redor de um domínio de negócio específico ([[Bounded Context]]).

Ao contrário do [[Arquitetura Monolítica|Monolito]], cada microserviço é desenvolvido, implantado e escalado independentemente.

## Funcionamento
A magia dos microserviços reside na independência:
- **Descentralização:** Cada serviço possui seu próprio banco de dados (idealmente) para evitar dependências ocultas.
- **Comunicação via Rede:** Serviços conversam entre si através de APIs leves (HTTP/REST ou gRPC) ou mensageria assíncrona.
- **Poliglotismo:** Um serviço de pagamento pode ser em Java, enquanto o de recomendação é em Python.

## Comparação
Microserviços vs. [[SOA]] (Service Oriented Architecture)

| Critério | Microservices | SOA (Tradicional) |
| :--- | :--- | :--- |
| **Granularidade** | Fina (Foco em função única). | Grossa (Foco em subsistemas inteiros). |
| **Compartilhamento** | "Share nothing" (Desacoplamento total). | Maximizar reuso de componentes (ESB). |
| **Comunicação** | Dumb pipes, smart endpoints. | Smart pipes (Barramento inteligente com lógica). |
| **Dados** | Decentralizados (Database-per-service). | Centralizados (Bancão compartilhado). |
