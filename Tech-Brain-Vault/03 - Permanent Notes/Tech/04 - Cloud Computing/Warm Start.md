---
created: 2026-02-10 11:29
updated: 2026-02-13 15:35
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Latência]]"
  - "[[Serverless Computing|Serverless]]"
  - "[[Cold Start]]"
aliases:
  - Inicialização Aquecida
---

## Definição
**Warm Start** ocorre quando uma função ou aplicação é executada em um ambiente que já foi previamente inicializado e ainda está ativo. Diferente de começar do zero, o sistema reaproveita recursos carregados na memória (contêineres, conexões de banco de dados, bibliotecas), resultando em uma execução quase instantânea.

## Funcionamento
- **Pré-existência:** Após uma primeira execução ([[Cold Start]]), o provedor de nuvem ou sistema mantém o ambiente "vivo" por um período determinado.
- **Nova Requisição:** Quando uma nova chamada chega dentro desse intervalo, ela é direcionada para esse ambiente pronto.
- **Execução Otimizada:** O código roda imediatamente, pois não há necessidade de alocar servidor, baixar código ou iniciar o runtime.

## Comparação
Warm Start vs [[Cold Start]]

| Característica | Warm Start                                | [[Cold Start]]                           |
| :------------- | :---------------------------------------- | :--------------------------------------- |
| **Latência**   | Baixíssima (ms).                          | Alta (pode levar segundos).              |
| **Recursos**   | Reutiliza contexto existente.             | Cria novo contexto do zero.              |
| **Custo**      | Geralmente incluído no tempo de execução. | Custo de tempo de "boot" inicial.        |
| **Ocorrência** | Tráfego constante ou frequente.           | Primeira requisição ou após inatividade. |