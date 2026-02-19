---
created: 2026-02-18 02:55
updated: 2026-02-18 02:55
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Control Structures]]"
aliases:
  - If-Else
  - Condicionais
  - Conditionals
  - Estruturas de Seleção
---

## Definição
**Selection Control** refere-se às estruturas de código que permitem ao programa tomar decisões e bifurcar seu fluxo de execução com base na avaliação de expressões booleanas (Verdadeiro ou Falso). É o mecanismo que confere "inteligência" e dinamicidade ao software.

## Funcionamento
O processador avalia uma condição lógica definida pelo programador.
- **Unidirecional (If)**: Executa um bloco apenas se a condição for verdadeira.
- **Bidirecional (If/Else)**: Escolhe entre dois caminhos exclusivos.
- **Multidirecional (Switch/Case/Elif)**: Seleciona um entre vários caminhos possíveis baseando-se no valor de uma variável.
Essas estruturas rompem a execução sequencial padrão do código.

## Comparação
Contrasta com as estruturas de **Iteration Control** (Loops como For/While), que repetem um bloco de código, e com a **Sequential Execution**, que segue linha por linha sem desvios. O uso excessivo de seleção aninhada (Nested Ifs) pode levar a uma complexidade ciclomática alta, dificultando a manutenção, diferente do **Polymorphism** em OOP que resolve decisões dinamicamente sem condicionais explícitas.