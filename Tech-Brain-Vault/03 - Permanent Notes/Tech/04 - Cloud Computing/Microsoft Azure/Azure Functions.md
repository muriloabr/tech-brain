---
created: 2026-02-03 14:32
updated: 2026-02-13 15:26
type: concept
status: 🌱
area: Tech
tags:
sources: []
related:
  - "[[Modelos de Serviço Cloud]]"
  - "[[Serverless Computing]]"
  - "[[Event-Driven Architecture]]"
---

## Definição
Serviço de computação [[Serverless Computing|Serverless]] do tipo [[FaaS]] (Function as a Service) da [[Microsoft Azure]]. Permite executar pequenos trechos de código (funções) em resposta a eventos, abstraindo totalmente o gerenciamento do servidor subjacente.

> [!info] Core Concept
> O foco sai da *infraestrutura* (onde roda) para a *lógica de negócio* (o que faz).

## Funcionamento
O **Azure Functions** opera sob uma arquitetura **[[Event-Driven Architecture|Orientada a Eventos]]** composta por dois elementos principais:
- **Gatilhos (Triggers):** O que *inicia* a execução. Uma função só pode ter um único gatilho.
    * *Exemplos:* Upload de arquivo no [[Azure Blob Storage]], Requisição HTTP (Webhook), Timer (Agendamento), Mensagem na [[Azure Queue Storage]].
- **Vínculos (Bindings):** Conexões declarativas com outros serviços para entrada (Input) ou saída (Output) de dados, sem precisar escrever código de conexão complexo.
    * *Exemplo:* Gravar o resultado direto no [[Cosmos DB]] usando um Output Binding.
### Planos de Hospedagem (Hosting Plans)
A forma como a função escala e é cobrada depende do plano escolhido:

* **Consumption Plan (Serverless Puro):**
    * Escala automaticamente de zero a milhares de instâncias.
    * Paga-se apenas pelo tempo de execução e memória (GB-s).
    * *Trade-off:* Pode sofrer com **[[Cold Start]]** (latência na primeira execução após inatividade).
* **Premium Plan:**
    * Mantém instâncias "aquecidas" (pre-warmed) para evitar Cold Start.
    * Permite conexão com VNet (Rede Virtual).
* **App Service Plan (Dedicado):**
    * Roda nas mesmas VMs que seus [[App Service - Azure|Web Apps]].
    * Custo previsível e fixo, mas não escala ao zero (você paga pela VM ligada 24/7).
### Cenários de Uso
- Processamento de arquivos em tempo real (ex: redimensionar imagem ao fazer upload).
- APIs leves e microsserviços.
- Automação de tarefas agendadas (Cron jobs).
- Integração de sistemas (ETL leve).

## Comparação
| Característica | **Azure Functions** | **[[App Service - Azure]] (Web App)** | **[[Azure Logic Apps]]** |
| :--- | :--- | :--- | :--- |
| **Foco** | Execução de código pontual (Eventos) | Hospedagem de Aplicações Web/API completas | Orquestração de workflows (Low-code) |
| **Estilo** | Code-first (Python, C#, JS) | Aplicação Contínua | Designer Visual (Arrastar blocos) |
| **Custo** | Por execução (Consumo) | Por hora (Reserva de instância) | Por ação executada |
