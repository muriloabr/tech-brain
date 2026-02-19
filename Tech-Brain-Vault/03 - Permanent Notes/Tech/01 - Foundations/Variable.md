---
created: 2026-02-13 20:37
updated: 2026-02-17 17:41
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Data Type]]"
  - "[[Scope]]"
aliases:
  - Variável
  - Identificador
---

## Definição
**Variable** (Variável) é uma abstração nomeada para um local na memória do computador. Ela permite que programadores armazenem, recuperem e manipulem dados utilizando nomes simbólicos legíveis (como `idade` ou `total`) em vez de precisarem gerenciar manualmente [[Memory Address|Endereços de Memória]] hexadecimais complexos.

## Funcionamento
Ao declarar uma variável (ex: `int x = 10`):
1.  **Reserva:** O compilador/interpretador solicita ao SO um bloco de memória do tamanho necessário para o tipo de dado (ex: 4 bytes para um inteiro).
2.  **Associação:** O nome `x` é vinculado ao endereço inicial desse bloco.
3.  **Manipulação:** Qualquer operação em `x` é traduzida pela máquina como uma operação no conteúdo daquele endereço de memória.

## Comparação
| Característica | Variável                         | Ponteiro (Pointer)                               |
| :------------- | :------------------------------- | :----------------------------------------------- |
| **Conteúdo**   | Armazena o dado em si (ex: `10`) | Armazena o endereço de outro dado (ex: `0xAB12`) |
| **Acesso**     | Direto ao valor                  | Indireto (precisa desreferenciar)                |
| **Abstração**  | Alto nível (fácil uso)           | Baixo nível (poderoso e perigoso)                |