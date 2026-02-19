---
created: 2026-02-12 17:37
updated: 2026-02-16 18:13
type: concept
status: 🌳
area: Tech
tags:
sources: []
related:
  - "[[Ética em IA]]"
aliases:
  - Inteligência Computacional
  - IA
  - Computational Intelligence
  - AI
---



# Definição
Ramo da [[Ciência da Computação]] dedicado ao [[Desenvolvimento de Sistemas]] capazes de executar tarefas que requerem inteligência humana. Envolve a **simulação de processos cognitivos** como aprendizado (aquisição de informação e regras), raciocínio (uso de regras para chegar a conclusões), autocorreção e percepção.

Não se limita a uma tecnologia isolada, mas atua como um campo abrangente que engloba teorias, métodos e algoritmos para emular capacidades biológicas em máquinas.

# Funcionamento
Opera fundamentalmente através do processamento de grandes volumes de dados ([[Big Data]]) combinados com algoritmos de processamento rápido e iterativo. 

O ciclo básico consiste em **Treinamento** (o sistema analisa dados para encontrar padrões), **Modelagem** (criação de um modelo matemático) e **Inferência** (aplicação do modelo em novos dados para predição ou decisão).

O campo divide-se em subáreas técnicas e camadas de complexidade:
- **[[Machine Learning]] (Aprendizado de Máquina):** Subconjunto onde computadores aprendem sem serem explicitamente programados para cada regra. Utiliza métodos estatísticos para melhorar o desempenho com a experiência.
	-  **Supervised Learning (Aprendizado Supervisionado):**
	    * O modelo treina com dados rotulados (input + output correto conhecido).
	    * *Exemplo:* Ensinar o modelo a reconhecer gatos mostrando fotos legendadas como "gato".
	* **Unsupervised Learning (Aprendizado Não-Supervisionado):**
	    * O modelo explora dados não rotulados para encontrar padrões ocultos ou estruturas intrínsecas.
	    * *Uso:* Vital para [[IA Generativa]], permitindo que o modelo aprenda a estrutura da linguagem ou imagens sem instruções rígidas.
	* **Reinforcement Learning (Aprendizado por Reforço):**
	    * O modelo aprende por tentativa e erro, recebendo "recompensas" ou "penalidades" baseadas em suas ações.
- **[[Deep Learning]] (Aprendizado Profundo):** Evolução do [[Machine Learning|ML]] que utiliza Redes Neurais Artificiais com múltiplas camadas para processar dados complexos (imagens, áudio) de forma não linear.
- **[[Processamento de Linguagem Natural]] (PLN/NLP):** Capacidade de entender, interpretar e gerar linguagem humana (chatbots, tradução).
- **[[Visão Computacional]]:** Extração de informações de imagens e vídeos (reconhecimento facial, diagnóstico médico).

# Comparação
| Característica          | Software Tradicional                    | Inteligência Artificial                             |
| :---------------------- | :-------------------------------------- | :-------------------------------------------------- |
| **Lógica**              | Determinística (If/Then/Else)           | Probabilística e Estatística                        |
| **Criação de Regras**   | Programador define regras explícitas    | Algoritmo deduz regras a partir dos dados           |
| **Tratamento de Dados** | Estruturados e previsíveis              | Estruturados e não estruturados (texto, vídeo)      |
| **Adaptação**           | Estática (requer atualização de código) | Dinâmica (aprende com novos dados)                  |
| **Resultado**           | Saída exata e constante                 | Melhor aproximação ou previsão (com margem de erro) |
