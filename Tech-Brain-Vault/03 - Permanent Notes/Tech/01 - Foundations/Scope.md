---
created: 2026-02-13 21:08
updated: 2026-02-13 21:10
type: concept
status: 🌱
area: Tech
tags: []
sources: []
related:
  - "[Variable, Call Stack, Memory Management]"
aliases:
- Escopo
- Visibilidade
- Variable Scope
---

## Definição
**Scope** (Escopo) é o contexto delimitado onde uma variável ou função é reconhecida e pode ser acessada pelo código. Ele define a visibilidade e o tempo de vida (lifetime) dos dados. Variáveis fora do seu escopo são "invisíveis" ou deixam de existir, o que é fundamental para evitar conflitos de nomes e economizar memória na Stack.

## Funcionamento
O escopo é gerenciado hierarquicamente:
1.  **Escopo Local (Function/Block):** Variáveis criadas dentro de uma função existem apenas enquanto ela executa (vivem na Stack Frame).
2.  **Escopo Global:** Variáveis acessíveis por todo o programa (vivem na área de dados estáticos ou Heap), geralmente desencorajadas por dificultarem o rastreamento de estado.
3.  **Escopo Léxico (Closure):** Funções internas podem acessar variáveis da função "pai", mesmo após o pai ter terminado (comum em JS e Funcional).

## Comparação
| Tipo | Escopo de Bloco (Block Scope) | Escopo de Função (Function Scope) |
| :--- | :--- | :--- |
| **Delimitador** | Chaves `{ ... }` (if, for, while) | Corpo da Função `func() { ... }` |
| **Linguagens** | C, Java, C#, JS (let/const) | JS Antigo (var), Python (parcialmente) |
| **Segurança** | Alta (variável morre rápido) | Média (variável vive até fim da função) |