---
created: 2026-02-13 21:19
updated: 2026-02-13 21:24
type: concept
status: 🌱
area: Tech
tags: []
sources: []
related:
  - "[Variable, Memory Address, Bit]"
aliases:
  - Tipo De Dado
  - Tipagem
  - Data Typing
---

## Definição
**Data Type** (Tipo de Dado) é um atributo que diz ao compilador ou interpretador como ele deve interpretar os bits armazenados em um endereço de memória. Como a memória guarda apenas zeros e uns, o "Tipo" define se aquela sequência binária representa um número inteiro, uma letra, um ponto flutuante ou uma estrutura complexa, além de determinar quanto espaço (bytes) ela ocupará.

## Funcionamento
O tipo impõe regras semânticas e estruturais:
1.  **Alocação:** Define o tamanho do bloco (ex: `int` costuma usar 4 bytes, `char` usa 1 byte).
2.  **Operação:** Define o que pode ser feito com o dado (ex: não faz sentido multiplicar "texto" por "texto").
3.  **Codificação:** Define o padrão de leitura (ex: IEEE 754 para floats, ASCII/UTF-8 para caracteres).

## Comparação
| Sistema de Tipos | Tipagem Estática (Static) | Tipagem Dinâmica (Dynamic) |
| :--- | :--- | :--- |
| **Verificação** | Tempo de Compilação (Compile-time) | Tempo de Execução (Runtime) |
| **Declaração** | Explícita (`int x = 10`) | Implícita (`x = 10`) |
| **Segurança** | Alta (pega erros antes de rodar) | Menor (pode quebrar no meio do uso) |
| **Exemplos** | Java, C++, TypeScript, Go | Python, JavaScript, Ruby |