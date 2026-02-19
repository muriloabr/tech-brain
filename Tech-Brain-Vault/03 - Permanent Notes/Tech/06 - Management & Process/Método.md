---
created: 2026-02-10 10:35
updated: 2026-02-13 15:37
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Classes]]"
  - "[[Encapsulation]]"
  - "[[Polymorphism]]"
aliases:
  - Method
  - Member Function
  - Métodos
---

## Definição
Em programação orientada a objetos ([[POO]]), um **Method** (Método) é uma subrotina ([[Função]]) que pertence a uma classe ou objeto. Ele define o **comportamento** dos objetos criados a partir daquela classe. Diferente de uma função isolada, o método tem acesso implícito aos dados internos (estado) do objeto através de palavras-chave como `this` ou `self`.

## Funcionamento
O método opera dentro do contexto de encapsulamento:
- **Associação:** É definido dentro do escopo de uma classe.
- **Acesso ao Estado:** Pode ler e modificar atributos da instância que o invocou (ex: `usuario.alterarSenha()` altera a senha daquele usuário específico).
- **Visibilidade:** Pode ser controlado por modificadores de acesso (Public, Private, Protected) para restringir quem pode invocá-lo.

## Comparação
Distinção técnica entre Método e Função (Frequentemente confundidos).

| Característica | Method                            | [[Função\|Function]]                            |
| :------------- | :-------------------------------- | :---------------------------------------------- |
| **Vínculo**    | Associado a um Objeto/Classe      | Independente (Standalone)                       |
| **Contexto**   | Possui contexto (`this`/`self`)   | Contexto apenas global ou passado via argumento |
| **Dados**      | Manipula estado interno do objeto | Manipula apenas entradas e saídas explícitas    |
| **Chamada**    | `objeto.metodo()`                 | `funcao()`                                      |
| **Paradigma**  | Orientação a Objetos              | Procedural / Funcional                          |

