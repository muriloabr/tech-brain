---
created: 2026-02-09 16:05
updated: 2026-02-13 15:38
type: concept
status: 🌿
area: Tech
tags:
sources:
  - "[[Core Competency]]"
  - "[[Technical Debt]]"
  - "[[Talent Acquisition]]"
related: []
aliases:
  - Desenvolvimento Interno
  - Internal Development
  - House Development
---

## Definição
**In-house Build** (ou Desenvolvimento Interno) é a estratégia de criar, manter e evoluir software ou soluções tecnológicas utilizando a equipe própria da organização, em vez de contratar terceiros ([[Outsourcing]]) ou comprar produtos prontos ([[Off-the-shelf]]).

É o ato de assumir a responsabilidade total pela engenharia do produto, transformando a empresa não apenas em uma consumidora de tecnologia, mas em uma produtora de tecnologia proprietária.

## Funcionamento
O In-house Build exige a estruturação de um departamento de tecnologia completo:
- **Talent Acquisition:** Recrutamento, contratação e retenção de engenheiros, designers e gerentes de produto (folha de pagamento).
- **Infraestrutura e Ferramentas:** Gestão de servidores, licenças de IDEs, [[Pipelines CI-CD]] e ambientes de desenvolvimento.
- **Gestão do Conhecimento:** A inteligência do negócio e o "como fazer" permanecem dentro da empresa, evitando a fuga de capital intelectual.
- **Ciclo de Vida ([[SDLC]]):** A equipe interna é responsável desde a concepção até a aposentadoria do software, incluindo correções de bugs e plantões (on-call).

## Comparação
In-house Build vs. [[Outsourcing]](Terceirização)

| Critério                     | In-house Build (Equipe Própria)                       | Outsourcing (Fábrica de Software)                             |
| :--------------------------- | :---------------------------------------------------- | :------------------------------------------------------------ |
| **Controle Cultural**        | Alto (Alinhamento total com a missão da empresa).     | Baixo (Cultura da contratada).                                |
| **Retenção de Conhecimento** | Alta (O conhecimento fica na casa).                   | Baixa (O conhecimento sai com o fim do contrato).             |
| **Custo a Longo Prazo**      | Geralmente menor para Core Business (Salários fixos). | Geralmente maior (Margem de lucro da contratada).             |
| **Flexibilidade de Escopo**  | Alta (Pivots são mais rápidos).                       | Baixa (Depende de renegociação contratual - Change Requests). |

