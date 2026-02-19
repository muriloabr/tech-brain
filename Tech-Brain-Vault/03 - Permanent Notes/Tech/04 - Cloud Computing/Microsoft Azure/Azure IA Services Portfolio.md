---
created: 2026-02-11 21:21
updated: 2026-02-13 22:21
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[IA Generativa]]"
  - "[[Processando Linguagem Natural]]"
  - "[[Machine Learning Operations]]"
aliases:
  - Serviços de IA do Azure
  - Azure AI Portfolio
---

## Definição
Conjunto de serviços em nuvem da Microsoft projetados para democratizar e implementar inteligência artificial, variando de modelos pré-treinados prontos para uso ([[SaaS]]) até plataformas robustas para desenvolvimento e treinamento de modelos personalizados ([[PaaS]]).

## Funcionamento
A escolha do serviço depende do nível de controle desejado e da natureza da tarefa:
- **[[Azure OpenAI Service]]:** Acesso a LLMs avançados (GPT). Focado em *Generative AI* para criação de texto, resumos, código e conversação complexa.
- [[Azure Machine Learning]] (Azure ML):** Ambiente para cientistas de dados. Permite controle total sobre algoritmos para criar, treinar e implantar modelos proprietários com dados específicos.
- **[[Azure AI Services]] (antigo Cognitive Services):** APIs com modelos pré-treinados pela Microsoft. Ideal para *Commodity AI* (visão computacional, tradução, fala) sem necessidade de experiência em ciência de dados.
- **[[Azure Bot Service]]:** Framework dedicado exclusivamente à criação, gerenciamento e orquestração de interfaces de chat e assistentes virtuais.

**Contexto de Nuvem:**
- [[Escalabilidade em Nuvem|Escalabilidade]]:** Ajuste dinâmico de recursos computacionais para suportar o treino de modelos pesados.
- **Integração:** Conexão nativa com Logic Apps (automação) e Data Factory (movimentação de dados).

## Comparação

| Cenário / Necessidade                         | Serviço Recomendado            | Característica Chave             |
| :-------------------------------------------- | :----------------------------- | :------------------------------- |
| **GenAI** (Criar texto, código, resumir)      | **[[Azure OpenAI Service]]**   | Criatividade e NLP avançado      |
| **Ciência de Dados** (Treinar modelo próprio) | **[[Azure Machine Learning]]** | Controle total e customização    |
| **Tarefas Prontas** (Ver, Ouvir, Falar)       | **[[Azure AI Services]]**      | Modelo pré-treinado (Sem treino) |
| **Interface de Chat** (Assistente Virtual)    | **[[Azure Bot Service]]**      | Orquestração de conversas        |
