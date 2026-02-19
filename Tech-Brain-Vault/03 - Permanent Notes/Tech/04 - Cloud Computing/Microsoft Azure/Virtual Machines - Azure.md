---
created: 2026-02-03 14:25
updated: 2026-02-13 10:39
type: concept
status: 🌱
area: Tech
tags:
sources: []
related:
  - "[[Modelos de Serviço Cloud]]"
  - "[[Microsoft Azure|Azure]]"
  - "[[IaaS]]"
  - "[[Cloud Computing]]"
  - "[[Máquina Virtual]]"
---

## Definição
O **Azure Virtual Machines (VM)** é um serviço de computação sob demanda que fornece recursos de computação virtualizados. É o exemplo clássico de **IaaS**. Você obtém controle total sobre o sistema operacional (Windows ou Linux).

## Funcionamento
A Microsoft gerencia o **hardware físico** (virtualização), mas você é responsável por instalar, configurar e atualizar o SO e os softwares instalados nele.

## Comparação
* **Diferente de [[App Service - Azure]]:** Na VM você gerencia o SO e patches; no [[App Service - Azure]] (PaaS), a Microsoft gerencia isso para você. 
* **Diferente de Azure Functions:** A VM fica ligada o tempo todo (e cobrando); em [[03 - Permanent Notes/Tech/04 - Cloud Computing/Microsoft Azure/Azure Functions]] a Function é disparada por eventos.