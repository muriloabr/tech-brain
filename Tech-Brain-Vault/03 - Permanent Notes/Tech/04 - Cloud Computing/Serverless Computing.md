---
created: 2026-02-08 11:41
updated: 2026-02-13 15:29
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Microservices]]"
  - "[[Cold Start]]"
  - "[[Cloud Computing]]"
  - "[[Event-Driven Architecture]]"
  - "[[Vendor Lock-in]]"
  - "[[FinOps]]"
aliases:
  - Computação sem Servidor
  - Serverless
---

## Definição
**Serverless Computing** é um **modelo de execução** nativo de [[Cloud Computing|Computação em Nuvem]] em que o provedor gerencia **toda a infraestrutura** — incluindo provisionamento, manutenção, segurança, atualizações do sistema operacional, tolerância a falhas e escalabilidade automática — permitindo que o desenvolvedor foque apenas no código.  

O nome “serverless” não significa ausência de servidores, mas sim que o usuário **não precisa administrá-los**. 

A **cobrança** é baseada **estritamente** no consumo real de recursos (tempo de execução e memória) durante a invocação da função, e **não** por capacidade pré-reservada **ociosa**, sendo a expressão máxima do [[Pay-per-use]],  eliminando assim a necessidade de provisionamento prévio ou gerenciamento de ociosidade (*idle time*).

É o **modelo de computação** onde:
- você **não gerencia servidores**.
- não controla VMs.    
- não escala manualmente.    
- paga **só pelo uso**.

> O que causa confusão é que **muita gente usa “serverless” como sinônimo de [[FaaS]]**, mas isso é só um pedacinho do modelo.
> **Serverless computing** é o modelo.  
> Dentro dele existe [[FaaS]] (funções) e [[BaaS]] (serviços gerenciados).  
> Todo [[FaaS]] é serverless, mas serverless NÃO é só [[FaaS]].

Apesar do nome, servidores *existem*, mas são invisíveis para o desenvolvedor. O foco é exclusivamente na **lógica de negócio** (código) e não na administração de sistemas. É a evolução da computação como utility (como água ou luz: você só paga pelo que consome).

## Funcionamento
O modelo opera sob o paradigma de **execução sob demanda**:
- **Escala Zero:** A aplicação reside em estado de repouso (custo zero) até ser solicitada. 
- **Invocação:** Um gatilho ativa a função. 
- **Micro-Faturamento:** A cobrança é calculada com base na **quantidade de invocações** e na **duração da execução** (geralmente em milissegundos) multiplicada pela memória alocada.
- **Desalocação Imediata:** Ao fim do processo, os recursos desaparecem instantaneamente.
### Dentro deste modelo existem dois tipos principais:
#### [[FaaS]] (Functions as a Service)
- Execução de funções sob demanda.    
- Orientado a eventos.    
- Ex.: [[00 - Inbox/Azure Functions]], [[AWS Lambda]], [[Google Cloud Functions]].    

#### [[BaaS]] (Backend as a Service)
- Serviços totalmente gerenciados.    
- Não exigem código de servidor.    
- Ex.: banco serverless, autenticação, storage, fila, messaging etc.

Você apenas sobe o seu código. A nuvem decide em qual máquina rodar, escala se houver muitos acessos e desliga tudo quando o código termina de executar.

## Comparação
Diferenças entre o modelo tradicional (IaaS/VMs), Containers e Serverless:

| Característica       | Serverless                                       | IaaS                                                       | PaaS / Containers                                     |
| :------------------- | :----------------------------------------------- | :--------------------------------------------------------- | :---------------------------------------------------- |
| **Modelo de Custo**  | [[Pay-per-use]] por invocação + GB/segundo.      | [[Pay-as-you-go]] por hora/segundo de instância *ligada*. | Por recurso reservado (nó/container/hora).            |
| **Ociosidade**       | Custo Zero.                                      | Custa o valor cheio da instância.                          | Custa a capacidade reservada do cluster/plano.        |
| **Escalabilidade**   | Elástica e granular (escala por *request*).      | Baseada em Auto-Scaling Groups (lento).                    | Configurável (HPA), limitada ao tamanho do cluster.   |
| **Responsabilidade** | Lógica de Negócio.                               | Sistema Operacional + Runtime + App.                       | Configuração do Container + Aplicação.                |
| **Latência**         | Possível [[Cold Start]] (atraso na 1ª execução). | Baixa e previsível (servidor sempre ligado).               | Baixa (container geralmente pré-aquecido).            |
| **Estado**           | [[Stateless]] (sem estado persistente).          | [[Stateful]] (disco local persistente).                    | Efêmero por padrão, suporta [[Stateful]] via volumes. |
