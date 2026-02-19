---
created: 2026-02-06 17:21
updated: 2026-02-13 15:23
type: concept
status: 🌿
area: Tech
tags: []
sources: []
related: []
aliases:
  - SRM
  - Shared Responsibility Model
  - Responsabilidade Compartilhada
---

## Definição
O **Modelo de Responsabilidade Compartilhada** (**Shared Responsibility Model**) define quem é responsável por cada aspecto da segurança e gestão no ambiente de nuvem. O conceito central é: a segurança **da** nuvem é do **provedor** ([[Security of the Cloud]]), enquanto a segurança **na** nuvem é do **cliente** ([[Security in the Cloud]]).

### A Divisão de Tarefas
A responsabilidade do cliente muda drasticamente dependendo do [[Modelos de Serviço Cloud|Modelo de Serviço]] escolhido:
 **Responsabilidade do Provedor (Sempre):**
    - Segurança física dos Data Centers (câmeras, guardas).
    - Infraestrutura de hardware (servidores, discos).
    - Infraestrutura de rede (cabos, roteadores).
    - Virtualização (Hypervisor).
 **Responsabilidade do Cliente (Sempre):**
    - **Dados:** Classificação, proteção e criptografia.
    - **Endpoints:** Dispositivos que acessam a nuvem.
    - **Contas e Identidades:** Gestão de quem tem acesso ([[IAM]]).

## Funcionamento

### Responsável de cada ambiente

| **Recurso**         | [[Infraestrutura Tradicional\|On-Premises]] | **[[IaaS]]** | **[[PaaS]]** | **[[SaaS]]**       |
| ------------------- | ------------------------------------------- | ------------ | ------------ | ------------------ |
| Dados               | Cliente                                     | Cliente      | Cliente      | Cliente            |
| Aplicações          | Cliente                                     | Cliente      | Cliente      | **Misto/Provedor** |
| Sistema Operacional | Cliente                                     | Cliente      | **Provedor** | **Provedor**       |
| Rede Física         | Cliente                                     | **Provedor** | **Provedor** | **Provedor**       |

## Comparação

