---
created: 2026-02-12 15:42
updated: 2026-02-13 16:46
type: concept
status: 🌳
area: Tech
tags:
sources: []
related:
  - "[[IA Generativa]]"
  - "[[Cybersecurity]]"
  - "[[Data Governance]]"
aliases:
  - GenAI Ethics & Limitations
  - Viés Algorítmico
  - Alucinação de IA
---

## Definição
**GenAI Ethics & Limitations** é um conjunto de desafios críticos e responsabilidades associados à implementação de IA Generativa.

Envolve a mitigação de riscos técnicos (alucinações), sociais (viés e deslocamento de trabalho) e legais (privacidade e propriedade intelectual), exigindo governança robusta e supervisão humana ("Human-in-the-loop").

## Funcionamento
Os riscos manifestam-se devido à natureza probabilística e dependente de dados dos modelos:
* **Natureza "Black Box" (Caixa Preta):** Falta de transparência sobre como o modelo chegou a uma conclusão, dificultando a auditoria e a confiabilidade em setores críticos (saúde/finanças).
* **Viés Algorítmico (Bias):** Se os dados de treinamento contêm preconceitos históricos (ex: discriminação em contratação), a IA irá amplificar esses padrões.
* **Alucinações:** A IA gera respostas plausíveis, porém factualmente incorretas ou inventadas, pois prioriza a coerência sintática sobre a verdade factual.
* **Privacidade e Vazamento:** Risco de modelos treinados reterem e exporem dados sensíveis ou proprietários inseridos pelos usuários.

## Comparação
Impacto da ausência versus presença de frameworks éticos na adoção de IA.

| Cenário | Consequência Negativa (Risco) | Medida de Mitigação (Ética) |
| :--- | :--- | :--- |
| **Saúde Mental** | Chatbot sugerindo autolesão (ex: caso GPT-3) por falta de compreensão emocional. | **Guardrails** rigorosos e encaminhamento humano para tópicos sensíveis. |
| **Recrutamento (RH)** | IA descartando candidatos de certas demografias baseada em histórico enviesado. | **Auditoria de Viés** nos datasets e anonimização de dados antes do treinamento. |
| **Operações** | Decisões automatizadas erradas sem explicação lógica (Black Box). | **Explicabilidade (XAI)** e transparência sobre o uso de IA para o usuário final. |
