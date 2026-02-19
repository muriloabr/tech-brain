---
created: 2026-02-13 20:35
updated: 2026-02-13 20:40
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related: []
aliases:
  - Endereço de Memória
  - Hex Address
  - Endereçamento
  - Endereços de Memória
---

## Definição
**Memory Address** (Endereço de Memória) é um identificador numérico único (geralmente representado em hexadecimal, ex: `0x7fff5fbff`) que localiza um byte específico na memória RAM do sistema. É a coordenada exata que a [[CPU]] utiliza para rastrear onde cada dado ou instrução está armazenado fisicamente.

## Funcionamento
O endereçamento opera como um sistema de CEPs para o hardware:
1.  **Mapeamento:** O Sistema Operacional mapeia a memória física em um espaço de endereçamento virtual para cada processo.
2.  **Acesso:** Quando um programa precisa de uma variável, ele não busca pelo "nome", mas consulta o endereço associado a ela.
3.  **Barramento:** A [[CPU]] envia esse número pelo Barramento de Endereços (Address Bus) para ativar a célula correspondente na memória.

## Comparação
| Conceito | Memory Address (Endereço) | Value (Valor) |
| :--- | :--- | :--- |
| **Analogia** | O número da caixa de correio | A carta dentro da caixa |
| **Representação** | Hexadecimal (`0x7A3F`) | Binário/Decimal/Char (`42`, `"A"`) |
| **Imutabilidade** | Fixo (para aquela alocação) | Variável (o conteúdo muda) |