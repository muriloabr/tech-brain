---
created: 2026-02-10 11:26
updated: 2026-02-13 15:29
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Microserviços]]"
  - "[[Cloud Computing]]"
  - "[[Escalabilidade em Nuvem|Escalabilidade]]"
aliases:
  - Sem Estado
---

## Definição
**Stateless** descreve um modelo de comunicação onde cada requisição é tratada como uma transação independente e isolada. O servidor não mantém nenhum registro ou "memória" das requisições anteriores; toda a informação necessária para processar o pedido deve vir contida na própria requisição feita pelo cliente.

## Funcionamento
- **Requisição Completa:** O cliente envia um pacote de dados que contém autenticação, estado desejado e comandos.
- **Processamento Isolado:** O servidor recebe, processa a informação baseando-se apenas no que recebeu naquele instante e devolve a resposta.
- **Descarte:** Após a resposta, o servidor "esquece" a interação.
- **Independência:** Não importa qual servidor do cluster atenda a requisição, pois nenhum deles segura o dado do usuário localmente.

## Comparação
Stateless vs [[Stateful]]

| Característica        | Stateless (Sem Estado)                | [[Stateful]] (Com Estado)                            |
| :-------------------- | :------------------------------------ | :--------------------------------------------------- |
| **Dependência**       | Nenhuma entre requisições.            | Alta dependência do histórico da sessão.             |
| **Carga no Servidor** | Menor uso de memória RAM por usuário. | Maior uso de recursos para manter sessões abertas.   |
| **Recuperação**       | Fácil recuperação de falhas.          | Requer mecanismos complexos de replicação de estado. |
| **Uso Ideal**         | Microserviços, APIs Públicas.         | Jogos Online, Bancos de Dados, Aplicações Legadas.   |