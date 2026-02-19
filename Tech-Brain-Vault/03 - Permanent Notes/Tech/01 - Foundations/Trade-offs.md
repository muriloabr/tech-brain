---
created: 2026-02-09 17:08
updated: 2026-02-13 15:33
type: concept
status: 🌳
area: Tech
tags:
sources: []
related:
  - "[[Pareto Principle]]"
  - "[[Opportunity Cost]]"
aliases:
  - Custo-Benefício
  - Compromissos de Projeto
  - Trocas
---

## Definição
**Trade-off** é uma decisão situacional que envolve perder uma qualidade ou aspecto de algo em troca de ganhar outro qualidade ou aspecto. Em engenharia de software, parte-se do princípio que "não existe bala de prata": toda solução técnica traz consigo uma desvantagem inerente.

## Funcionamento
A análise de trade-offs funciona balanceando forças opostas:

* **Velocidade vs. Qualidade:** Entregar rápido (Ganha [[Time-to-Market]]) vs. Código limpo (Ganha [[Maintainability]]).
* **Consistência vs. Disponibilidade:** [[Teorema CAP]] (Em sistemas distribuídos, é impossível ter [[Consistência forte]] e [[Alta Disponibilidade]] ao mesmo tempo durante uma partição).
* **Flexibilidade vs. Simplicidade:** Sistemas muito configuráveis são difíceis de usar e manter.

## Comparação
Solução Ideal vs. Solução Pragmática

| Critério | Solução Ideal (Teórica) | Solução Pragmática (Real) |
| :--- | :--- | :--- |
| **Objetivo** | Maximizar todos os parâmetros. | Otimizar o parâmetro crítico para o negócio. |
| **Custo** | Infinito (Impossível de atingir). | Viável. |
| **Mentalidade** | "Melhor possível". | "Bom o suficiente para agora". |
| **Contexto** | Ignora restrições. | Baseada em restrições (tempo, dinheiro, equipe). |