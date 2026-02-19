---
created: 2026-02-09 16:09
updated: 2026-02-13 15:39
type: concept
status: 🌳
area: Tech
tags:
sources:
related:
  - "[[Business Process Management]]"
  - "[[Automation]]"
  - "[[Standard Operating Procedure]]"
aliases:
  - Fluxo de Trabalho
  - Fluxos
  - Fluxo
---

## Definição
**Workflows** (Fluxos de Trabalho) são sequências orquestradas e repetíveis de tarefas, processos ou dados que passam de uma etapa para outra até a conclusão de um objetivo específico.

Um workflow não é apenas uma lista de tarefas (to-do list), mas sim a definição estruturada de "como", "quando" e "por quem" o trabalho flui dentro de um sistema ou equipe.

## Funcionamento
Um workflow opera através de uma lógica de estados e transições:
* **Gatilho ([[Event Trigger]]):** O evento que inicia o fluxo (ex: recebimento de um e-mail, preenchimento de formulário).
* **Etapas (Steps):** As ações que devem ser realizadas (humanas ou automatizadas).
* **Regras de Negócio:** Condicionais que ditam o caminho (ex: "Se o valor for > 1000, requer aprovação do gerente").
* **Saída (Output):** O resultado final entregável ou a mudança de estado no sistema.

## Comparação
Workflow vs. [[Ad-hoc]](Improviso)

| Critério                | Workflow Estruturado                       | Processo Ad-hoc                                 |
| :---------------------- | :----------------------------------------- | :---------------------------------------------- |
| **Previsibilidade**     | Alta (Sabe-se exatamente o próximo passo). | Baixa (Depende da decisão momentânea).          |
| **Eficiência**          | Otimizável e mensurável.                   | Variável e difícil de rastrear.                 |
| **Dependência Pessoal** | Baixa (O processo guia a pessoa).          | Alta (O conhecimento está na cabeça da pessoa). |
| **Automação**           | Altamente automatizável.                   | Difícil ou impossível de automatizar.           |
| **Qualidade**           | Consistente.                               | Flutuante.                                      |
