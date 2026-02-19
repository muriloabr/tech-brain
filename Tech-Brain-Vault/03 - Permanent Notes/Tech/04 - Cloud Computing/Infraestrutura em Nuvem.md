---
created: 2026-02-10 10:07
updated: 2026-02-13 15:37
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[DevOps]]"
  - "[[Data Center]]"
  - "[[03 - Permanent Notes/Tech/03 - Infrastructure & Systems/Virtualization]]"
aliases:
  - Infraestrutura em Nuvem
  - Cloud Infrastructure
---

## Definição
**Cloud Infrastructure** é o conjunto de componentes físicos e lógicos que compõem a base da computação em nuvem. Inclui datacenters, servidores, armazenamento, redes físicas, mecanismos de virtualização e camadas de abstração que permitem que provedores disponibilizem recursos computacionais de forma elástica, automatizada e acessível via Internet.

É a **infraestrutura que existe por trás dos serviços de nuvem**, não o modelo de consumo (como [[IaaS]], [[PaaS]] ou [[SaaS]]).

## Funcionamento
A infraestrutura em nuvem opera por meio de **camadas de abstração**, **virtualização avançada** e **orquestração automatizada**, permitindo que múltiplos serviços sejam executados simultaneamente sobre o mesmo hardware físico.
- **Virtualização:** Hypervisors e tecnologias de containerização isolam workloads, permitindo que vários ambientes rodem no mesmo hardware.
- **Orquestração:** Sistemas internos do provedor distribuem cargas, monitoram recursos e garantem disponibilidade, resiliência e elasticidade.
- **Camadas de API:** A infraestrutura expõe capacidades internas por meio de APIs usadas pelos serviços da nuvem (incluindo [[IaaS]], [[PaaS]], [[FaaS]] e [[SaaS]]).

  *O usuário final raramente interage diretamente com a infraestrutura em si — ele consome modelos como [[IaaS]] que utilizam essa infraestrutura.*

## Comparação
Comparativo entre a **Infraestrutura em Nuvem** (a base operacional dos provedores) e a **Infraestrutura Tradicional** (mantida localmente).

| Característica      | Cloud Infrastructure                                                                                                    | [[Infraestrutura Tradicional\|On-Premise Infrastructure]] |
| :------------------ | :---------------------------------------------------------------------------------------------------------------------- | :-------------------------------------------------------- |
| **Modelo de Custo** | [[OpEx]] (Custos operacionais, alto aproveitamento e eficiência interna do provedor)                                    | [[CapEx]] (Compra e renovação de hardware)                |
| **Escalabilidade**  | Elástica e automatizada internamente pelos provedores                                                                    | Limitada ao hardware adquirido                            |
| **Manutenção**      | Totalmente sob responsabilidade do provedor (datacenters, hardware, rede, energia, virtualização)                        | Equipe interna de TI realiza toda manutenção física e lógica |
| **Acesso**          | Infraestrutura global, distribuída e redundante, acessível pelos serviços expostos na nuvem                              | Acesso depende do ambiente físico local                   |
| **Implementação**   | Provisionamento interno altamente automatizado e padronizado                                                             | Instalação física manual e lenta                          |
