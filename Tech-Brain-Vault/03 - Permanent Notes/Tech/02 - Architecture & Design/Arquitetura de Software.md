---
created: 2026-02-09 16:23
updated: 2026-02-13 15:30
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Design Patterns]]"
  - "[[Escalabilidade em Nuvem|Escalabilidade]]"
  - "[[Domain-Driven Design]]"
aliases:
  - System Architecture
  - Arquitetura de Sistemas
  - Software Architecture
---

## Definição
**Software Architecture** refere-se às estruturas fundamentais de um sistema de software e à disciplina de criar tais estruturas. Ela define as decisões de design de alto nível que são difíceis e custosas de mudar posteriormente (os "ossos" do sistema), envolvendo a escolha de componentes, suas interações e as restrições que regem o projeto.

## Funcionamento
A arquitetura lida com [[Trade-offs]](Trocas):

1.  **Padrões Arquiteturais:** Escolha do modelo base (ex: [[Arquitetura Monolítica]], [[Microserviços]], [[Event-Driven Architecture]]).
2.  **Atributos de Qualidade ([[Requisitos Não Funcionais]]):** Focar em requisitos não funcionais como segurança, performance e manutenibilidade.
3.  **Limites:** Define o que cada parte do sistema deve e não deve fazer (Separação de Responsabilidades).

## Comparação
Arquitetura vs. [[Design de Software]]

| Critério | Arquitetura | Design |
| :--- | :--- | :--- |
| **Nível** | Macro (Alto Nível). | Micro (Baixo Nível). |
| **Escopo** | Sistema inteiro e integração entre módulos. | Classes, funções e estrutura interna de módulos. |
| **Decisões** | Estruturais (Banco de dados, Linguagem, Framework). | Implementação (Algoritmos, Padrões de Código). |
| **Visibilidade** | Stakeholders técnicos e de negócio. | Desenvolvedores. |
| **Impacto de Mudança** | Catastrófico (Reescrever o sistema). | Localizado (Refatorar uma classe). |