---
created: 2026-02-09 16:00
updated: 2026-02-13 15:37
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Multi-cloud Strategy]]"
  - "[[Migration Cost]]"
  - "[[]]"
  - "[[Interoperability]]"
aliases:
  - Lock-in
  - Aprisionamento Tecnológico
---

## Definição
**Vendor Lock-in** descreve uma situação em que um cliente se torna dependente de um fornecedor (vendor) de produtos ou serviços e não pode mudar para outro concorrente sem custos substanciais de troca, complexidade técnica extrema ou interrupção do negócio.

É o fenômeno de ficar "preso" a uma tecnologia proprietária, onde o custo de sair é maior do que o benefício de mudar.

## Funcionamento
O Lock-in acontece através de barreiras criadas (intencionalmente ou não) pelo fornecedor:
-  **Formatos Proprietários:** Dados salvos em formatos que outros softwares não leem.
- **Integração Profunda:** O sistema da empresa é construído usando APIs exclusivas daquele fornecedor.
- **Custos de Saída ([[Egress Fees]]):** Cobrança alta para retirar dados da plataforma (comum em Cloud).
- **Curva de Aprendizado:** A equipe treinou anos naquela ferramenta específica e reaprender outra seria custoso.

## Comparação
Vendor Lock-in vs. [[Open Standards]](Padrões Abertos)

| Critério | Vendor Lock-in | Open Standards |
| :--- | :--- | :--- |
| **Liberdade de Escolha** | Restrita ao ecossistema do fornecedor. | Total (pode trocar de ferramenta mantendo o padrão). |
| **Custo de Migração** | Proibitivo ou muito alto. | Baixo ou moderado. |
| **Inovação** | Depende do roadmap do fornecedor. | Pode integrar inovações de múltiplas fontes. |
| **Controle de Dados** | Difícil (os dados "moram" lá). | Fácil (os dados são portáveis). |
| **Pod
