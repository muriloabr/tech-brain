---
created: 2026-02-03 14:16
updated: 2026-02-13 15:39
type: concept
status: 🌱
area: Tech
tags:
sources:
  - https://azure.microsoft.com/en-us/products/app-service
related:
  - "[[Modelos de Serviço Cloud]]"
---

## Definição
O **Azure App Service** é um serviço baseado em HTTP para hospedagem de aplicações web, APIs REST e backends para dispositivos móveis. É uma oferta clássica de **PaaS (Platform as a Service)**.

## Funcionamento
Ele abstrai toda a infraestrutura subjacente. Você **não** gerencia o **servidor**, nem o **Sistema Operacional**, nem os **patches de segurança**. 
* **Suporte a Linguagens:** .NET, .NET Core, Java, Ruby, Node.js, PHP ou Python.
* **Escalabilidade:** Permite *Scale Up* (mais potência na máquina) e *Scale Out* (mais cópias da máquina) manual ou automático.
* **Slots de Implantação:** Permite criar ambientes de "**Staging**" para testar antes de jogar para "**Production**".

## Comparação
* **Diferente de [[Virtual Machines - Azure]] (IaaS):** Na VM, você precisa instalar o IIS/Apache, configurar o firewall e atualizar o Windows/Linux. No App Service, isso é automático. 
* **Diferente de Azure Functions (Serverless):** O App Service é focado em aplicações que rodam continuamente, enquanto Functions são para códigos disparados por eventos (triggers).
