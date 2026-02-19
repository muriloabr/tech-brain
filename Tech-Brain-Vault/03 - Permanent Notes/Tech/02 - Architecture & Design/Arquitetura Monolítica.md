---
created: 2026-02-09 16:45
updated: 2026-02-13 15:34
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Escalabilidade em Nuvem|Escalabilidade]]"
  - "[[Pipelines CI-CD|CI/CD]]"
  - "[[Refatoração]]"
aliases:
  - Monolito
  - Monolith
  - Arquitetura Monolítica
  - Monolithic Architecture
---

## Definição
**Monolithic Architecture** é um modelo tradicional de [[Design de Software]] onde a aplicação é construída como uma unidade única, indivisível e autossuficiente.

Neste modelo, todas as funcionalidades (interface do usuário, lógica de negócios e acesso a dados) residem no mesmo código-fonte (codebase) e são implantadas juntas. Se uma parte do sistema precisa mudar, todo o sistema deve ser recompilado e reimplantado.

## Funcionamento
O Monolito opera sob o princípio de acoplamento forte:
- **Codebase Único:** Todo o código está em um repositório.
- **Implantação Atômica:** É "tudo ou nada". Você não sobe apenas a atualização do carrinho de compras; você sobe a loja inteira.
- **Memória Compartilhada:** Módulos internos comunicam-se por chamadas de função diretas, compartilhando a mesma memória RAM e CPU da instância.

## Comparação
Arquitetura Monolítica vs. [[Arquitetura Modular]]

| Critério                 | Monolito                                   | Modular/Distribuído                         |
| :----------------------- | :----------------------------------------- | :------------------------------------------ |
| **Complexidade Inicial** | Baixa (Fácil de começar).                  | Alta (Infraestrutura complexa).             |
| **Debug**                | Simples (Rastreia tudo no mesmo lugar).    | Difícil (Rastreamento distribuído).         |
| **Escalabilidade**       | Vertical (Aumentar a máquina).             | Horizontal (Adicionar mais máquinas).       |
| **Falha**                | Cascata (Um erro de memória derruba tudo). | Isolada (Um serviço cai, o resto funciona). |
| **Tecnologia**           | Única (Preso a uma stack/linguagem).       | Agnóstica (Cada módulo pode ter sua stack). |