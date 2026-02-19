---
created: 2026-02-18 02:57
updated: 2026-02-18 02:57
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Boolean Algebra]]"
aliases:
  - Tabela Verdade
---

## Definição
A **Truth Table** é uma ferramenta matemática tabular utilizada para descrever funcionalmente a saída de um circuito lógico ou proposição composta para todas as combinações possíveis de valores de entrada. Ela representa exaustivamente o comportamento de operadores lógicos (AND, OR, NOT, XOR, etc.).

## Funcionamento
A tabela é construída listando todas as variáveis de entrada em colunas à esquerda e a saída resultante à direita.
- O número de linhas é determinado por $2^n$, onde $n$ é o número de variáveis de entrada.
- Cada linha representa um estado único do sistema (ex: 0 e 1, Verdadeiro e Falso).
É essencial para o design de circuitos digitais, depuração de condicionais complexas em programação e simplificação de expressões lógicas.

## Comparação
A Truth Table é a representação "extensiva" da lógica, listando todos os casos. 
Ela contrasta com as **Boolean Expressions** (representação algébrica compacta) e com os **Logic Gates Diagrams** (representação visual esquemática). Enquanto a álgebra permite manipulação simbólica, a tabela verdade oferece verificação absoluta e prova de equivalência lógica.