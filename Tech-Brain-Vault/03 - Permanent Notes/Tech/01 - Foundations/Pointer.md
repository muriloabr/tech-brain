---
created: 2026-02-13 20:30
updated: 2026-02-17 23:37
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Variable]]"
  - "[[Memory Management]]"
aliases:
  - Ponteiro
  - Memory Pointer
  - Endereço de Memória
---

## Definição
Um **Pointer** (Ponteiro) é um tipo especial de variável que armazena um endereço de memória hexadecimal, em vez de armazenar um valor de dados diretamente.

Ele atua como uma "seta" ou referência que aponta para onde o dado real está localizado na memória física (geralmente na [[Heap Memory|Heap]]). É a ferramenta fundamental para construção de estruturas de dados complexas e manipulação eficiente de recursos.

## Funcionamento
O ponteiro opera através de dois operadores principais (na sintaxe C/C++):
1.  **Referencing (&):** Obtém o endereço de uma variável existente (ex: "Onde o `x` mora?").
2.  **Dereferencing (*):** Acessa ou modifica o valor armazenado no endereço para o qual o ponteiro aponta (ex: "Vá até o endereço e pegue o que está lá").
Ponteiros permitem a "passagem por referência", onde uma função pode modificar a variável original de outra função sem precisar criar uma cópia dos dados, economizando memória e ciclos de [[CPU]].

## Comparação
| Característica | Pointer (Ponteiro) | Reference (Referência Moderna) |
| :--- | :--- | :--- |
| **Segurança** | Baixa (pode apontar para memória inválida/nula) | Alta (garantida de apontar para objeto existente) |
| **Aritmética** | Permitida (pode-se somar endereços para percorrer arrays) | Proibida (abstração fixa) |
| **Nulidade** | Pode ser `NULL` (vazio) | Geralmente não pode ser nula |
| **Uso** | C, C++, Assembly (Sistemas, Drivers) | Java, Python, C# (Aplicações de Alto Nível) |
