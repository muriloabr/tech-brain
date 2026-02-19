---
created: 2026-02-09 16:18
updated: 2026-02-13 15:28
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Provisioned Concurrency]]"
  - "[[FaaS]]"
  - "[[Containerization]]"
aliases:
  - Partida a Frio
---

## Definição
**Cold Start** refere-se ao atraso (latência) que ocorre quando uma [[Função FaaS|Função Serverless]] (como [[AWS Lambda]] ou [[Google Cloud Functions]]) é invocada pela primeira vez após um período de inatividade, ou quando o sistema precisa escalar para atender a um pico de tráfego.

O provedor de nuvem precisa alocar recursos, subir o container e carregar o código antes que a execução real comece.

## Funcionamento
O processo invisível ao usuário, mas sentido na performance:
- **Gatilho:** Uma requisição chega.
- **Verificação:** O provedor checa se há uma instância "quente" (já rodando) disponível.
- **Provisionamento (Cold):** Se não houver, ele baixa o código, inicia um novo container e configura o runtime (Java, Python, Node, etc.).
- **Execução:** O código roda e retorna a resposta.
- **Descarte:** Se ficar inativo por alguns minutos, o container é destruído para economizar recursos.

## Comparação
Cold Start vs. [[Warm Start]]

| Critério | Cold Start | Warm Start |
| :--- | :--- | :--- |
| **Latência** | Alta (Pode levar de 100ms a vários segundos). | Baixa (Milissegundos). |
| **Custo para o Provedor** | Alto (Alocação de novos recursos). | Baixo (Reuso de recursos). |
| **Ocorrência** | Primeira execução ou picos de escala. | Execuções subsequentes frequentes. |
| **Mitigação** | Manter funções "vivas" artificialmente (pings). | Tráfego constante. |