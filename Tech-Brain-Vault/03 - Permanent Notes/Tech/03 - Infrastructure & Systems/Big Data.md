---
created: 2026-02-16 18:16
updated: 2026-02-16 18:16
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Information Science]]"
  - "[[Database Management Systems]]"
  - "[[Statistics]]"
aliases:
  - Mega Dados
  - Grande Volume de Dados
---

## Definição
Termo que descreve conjuntos de dados cujo volume, velocidade ou variedade são tão grandes que dificultam ou impossibilitam sua captura, gerenciamento, processamento e análise utilizando tecnologias de banco de dados e ferramentas de software tradicionais. É a base para análises avançadas que revelam padrões ocultos e correlações.

## Funcionamento
Baseia-se no conceito dos "Vs" (Volume, Velocidade, Variedade, Veracidade, Valor) e em arquiteturas distribuídas:
1. **Ingestão:** Coleta de dados de múltiplas fontes (IoT, redes sociais, logs).
2. **Armazenamento:** Uso de Data Lakes ou sistemas de arquivos distribuídos (como HDFS) que permitem escalabilidade horizontal em clusters de servidores comuns.
3. **Processamento:** Computação paralela (como MapReduce ou Spark) onde a tarefa é dividida em fragmentos menores processados simultaneamente em diferentes nós.
4. **Análise:** Aplicação de algoritmos de mineração de dados ou Machine Learning sobre o conjunto massivo.

## Comparação
**Big Data vs. [[Bancos de Dados Relacionais]] (RDBMS)**
**RDBMS** são ideais para dados estruturados, consistentes e transacionais (ACID) com volume moderado e esquema fixo. **Big Data** é projetado para lidar com dados não estruturados ou semi-estruturados, volumes petabytes, alta velocidade de gravação e esquemas flexíveis (Schema-on-Read).