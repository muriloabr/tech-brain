---
created: 2026-02-09 15:55
updated: 2026-02-13 15:34
type: concept
status: 🌳
area: Tech
tags:
sources: []
related:
  - "[[Buy vs Build]]"
  - "[[SaaS]]"
  - "[[Licensing]]"
aliases:
  - COTS
  - De Prateleira
  - Commercial Off-The-Shelf
  - Solução Comercial
---

## Definição
**Off-the-shelf** (ou Commercial Off-The-Shelf - COTS) refere-se a produtos de software ou hardware que são fabricados e disponibilizados para o mercado de massa, prontos para serem usados imediatamente após a compra, sem a necessidade de desenvolvimento customizado. É a analogia de comprar um terno pronto em uma loja de departamento, em oposição a mandar fazer um sob medida em um alfaiate. O produto é desenhado para atender às necessidades de 80% do mercado, não aos caprichos específicos de um único cliente.

## Funcionamento
Soluções Off-the-shelf operam sob a lógica de economia de escala:
- **Padronização:** O fornecedor desenvolve um conjunto de funcionalidades que atende à maioria das empresas do setor.
- **Licenciamento:** O modelo de negócio geralmente envolve a venda de licenças de uso (perpétuas ou subscrição/SaaS).
- **Ciclo de Atualização:** As melhorias e correções de segurança são distribuídas simultaneamente para todos os clientes através de *patches* ou novas versões.
- **Configuração vs. Customização:** Permite ajustes de parâmetros (configuração), mas raramente permite alteração do código-fonte (customização profunda).

## Comparação
Off-the-shelf(Comprar) vs. [[In-house Build]](Construir)

| Critério                 | Off-the-shelf(COTS)                            | [[In-house Build]](Construir)               |
| :----------------------- | :--------------------------------------------- | :------------------------------------------ |
| **Time-to-Market**       | Imediato (Instalar e usar).                    | Lento (Desenvolver e testar).               |
| **Custo Previsível**     | Alto no [[OPEX]] (Licenças recorrentes).       | Alto no [[CAPEX]] (Salários e Infra).       |
| **Manutenção**           | Externa (Risco de descontinuação pelo vendor). | Interna (Risco de turnover da equipe).      |
| **Aderência**            | Genérica (Você adapta seu processo).           | Específica (O software adapta ao processo). |
| **Vantagem Competitiva** | Nula (Seu concorrente pode comprar o mesmo).   | Potencial (Se for o core business).         |
