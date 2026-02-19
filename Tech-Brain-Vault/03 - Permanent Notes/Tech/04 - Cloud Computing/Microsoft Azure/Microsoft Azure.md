---
created: 2026-02-05 21:27
updated: 2026-02-13 15:25
type: concept
status: 🌿
area: Tech
tags:
sources: []
related: []
aliases:
  - Azure
  - Plataforma Azure
---

## Definição
O **Azure** é a plataforma de [[Cloud Computing]] pública da [[Microsoft]].
É um conjunto massivo de [[Modelos de Serviço Cloud]] que permite criar, implantar e gerenciar aplicações através da rede global de datacenters da [[Microsoft]].

* **Modelo:** Pay-as-you-go (Paga apenas pelo que usa).
* **Foco de Mercado:** Muito forte no mercado corporativo (Enterprise) devido à integração nativa com produtos Microsoft (Windows Server, SQL Server, Active Directory).

## Funcionamento
O Azure não é apenas um "monte de servidores". Ele funciona com base em dois pilares principais: a **estrutura física** (onde estão os computadores) e a **estrutura lógica** (como você organiza suas coisas).

### Como o Azure processa seus pedidos? (ARM)
Tudo o que você faz no Azure (seja pelo Portal, CLI ou código) passa por uma camada central chamada **Azure Resource Manager (ARM)**.
* **O que ele faz:** Autentica você, verifica se você tem permissão e envia o comando para o serviço correto.
* **Benefício:** Permite usar "Templates" (IaC) para criar infraestrutura via código JSON.

### 2. Estrutura Física (Onde os dados vivem)
* **Datacenters:** Prédios físicos com servidores, refrigeração e energia própria.
* **Regiões (Regions):** Um conjunto de datacenters conectados dentro de um perímetro de latência (Ex: *Brazil South*, *East US*). Todo recurso precisa estar em uma região.
* **Zonas de Disponibilidade (Availability Zones):** Datacenters fisicamente separados *dentro* da mesma região. Se um prédio pegar fogo, o outro assume (proteção contra falhas de datacenter).
* **Pares de Regiões (Region Pairs):** Duas regiões conectadas para recuperação de desastres (Ex: Se o *Brazil South* cair totalmente, o *South Central US* pode ser o par de backup).

### 3. Estrutura Lógica (Como você organiza)
Para usar qualquer serviço, você precisa seguir esta hierarquia obrigatória:

1. **Tenant (Entra ID):** A identidade da sua empresa (sua conta).
2. **Management Groups:** (Opcional) Agrupa várias assinaturas para aplicar governança em empresas grandes.
3. **Assinatura (Subscription):** É aqui que ocorre o faturamento. Nada existe sem uma assinatura (onde você coloca o cartão de crédito).
4. **Resource Groups (Grupos de Recursos):** É um container lógico. **Todo** recurso (VM, Banco de Dados, VNet) deve pertencer a um único Resource Group.
    * *Regra de ouro:* Recursos que compartilham o mesmo ciclo de vida (nascem e morrem juntos) devem ficar no mesmo grupo.
5. **Recursos:** Os serviços em si (a VM, o Banco de Dados, etc).

Exemplos de serviços Azure:

| **Categoria**     | **Serviço**                         | **Modelo**        | **Descrição (Foco Exame AZ-900)**                                                              |
| ----------------- | ----------------------------------- | ----------------- | ---------------------------------------------------------------------------------------------- |
| **Computação**    | [[Virtual Machines - Azure]]        | IaaS              | Emulação de um computador físico (Windows/Linux). Controlo total do SO.                        |
| **Computação**    | [[VM Scale Sets - Azure]]           | IaaS              | Permite criar e gerir um grupo de VMs idênticas com autoscale (escalabilidade automática).     |
| **Computação**    | [[Availability Sets - Azure]]       | IaaS              | Garante redundância e disponibilidade das VMs (protege contra falhas de rack/atualizações).    |
| **Computação**    | [[App Service - Azure]]             | PaaS              | Hospedagem de aplicações Web (HTTP). Suporta .NET, Java, Node, etc. sem gerir servidores.      |
| **Computação**    | [[03 - Permanent Notes/Tech/04 - Cloud Computing/Microsoft Azure/Azure Functions]]               | PaaS (Serverless) | Computação orientada a eventos. Executa código (snippets) sem provisionar infraestrutura.      |
| **Computação**    | [[Azure Container Instances (ACI)]] | PaaS              | A forma mais rápida de rodar um contentor no Azure sem orquestração complexa.                  |
| **Computação**    | [[Azure Kubernetes Service (AKS)]]  | PaaS              | Orquestração de contentores (Kubernetes) gerida pela Microsoft.                                |
| **Computação**    | [[Azure Virtual Desktop]]           | PaaS/IaaS         | Virtualização de desktops e aplicações na nuvem (VDI).                                         |
| **Rede**          | [[Virtual Network (VNet)]]          | IaaS              | Rede privada no Azure. Isola recursos e permite comunicação segura.                            |
| **Rede**          | [[VPN Gateway - Azure]]             | IaaS              | Conecta a tua rede on-premises ao Azure através da internet pública (encriptado).              |
| **Rede**          | [[ExpressRoute-Azure]]              | IaaS              | Conexão privada e dedicada (fibra) entre a tua empresa e o Azure (não usa internet pública).   |
| **Rede**          | [[Load Balancer-Azure]]             | IaaS              | Distribui tráfego de rede (Layer 4) entre várias VMs (TCP/UDP).                                |
| **Rede**          | [[Application Gateway - Azure]]     | PaaS              | Balanceador de carga web (Layer 7) com Firewall de Aplicação Web (WAF).                        |
| **Rede**          | [[Azure DNS]]                       | PaaS              | Serviço de hospedagem de domínios DNS usando a infraestrutura do Azure.                        |
| **Armazenamento** | [[Blob Storage]]                    | PaaS              | Armazenamento de objetos massivos não estruturados (imagens, vídeos, backups).                 |
| **Armazenamento** | [[Disk Storage]]                    | IaaS              | Discos virtuais (HDD/SSD) acoplados a VMs.                                                     |
| **Armazenamento** | [[Azure Files]]                     | PaaS              | Partilha de ficheiros via protocolo SMB (acessível como drive de rede).                        |
| **Armazenamento** | [[Archive Storage]]                 | PaaS              | Camada de armazenamento de baixo custo para dados raramente acedidos (Long-term).              |
| **Base de Dados** | [[Azure SQL Database]]              | PaaS              | Versão totalmente gerida do SQL Server. Alta disponibilidade integrada.                        |
| **Base de Dados** | [[Cosmos DB]]                       | PaaS              | Base de dados NoSQL globalmente distribuída e multi-modelo (rápida e escalável).               |
| **Base de Dados** | [[D.B. for MySQL/PostgreSQL]]       | PaaS              | Bases de dados open-source geridas pela Microsoft.                                             |
| **Base de Dados** | [[SQL Managed Instance]]            | PaaS              | Facilita a migração "Lift and Shift" de SQL Servers on-premises para a nuvem.                  |
| **IoT**           | [[IoT Hub]]                         | PaaS              | Centro de mensagens para comunicação bidirecional entre milhões de dispositivos IoT e a nuvem. |
| **IoT**           | **IoT Central**                     | SaaS              | Solução pronta (dashboard) para monitorizar dispositivos IoT sem codificação complexa.         |
| **Big Data**      | **Azure Synapse Analytics**         | PaaS              | Data Warehousing e análise de Big Data unificados.                                             |
| **Big Data**      | **HDInsight**                       | PaaS              | Serviços de análise open-source (Hadoop, Spark, Kafka) geridos.                                |
| **Big Data**      | **Azure Databricks**                | PaaS              | Plataforma de análise baseada em Apache Spark (muito usada por Engenheiros de Dados).          |
| **IA / ML**       | **Azure Machine Learning**          | PaaS              | Ambiente para treinar, implementar e gerir modelos de Machine Learning.                        |
| **IA / ML**       | [[Azure AI Services]]               | PaaS/SaaS         | APIs prontas de IA (Visão, Fala, Linguagem) para developers (ex: Reconhecimento Facial).       |
| **Gestão**        | [[Azure Portal]]                    | Ferramenta        | Interface gráfica baseada na web para gerir o Azure.                                           |
| **Gestão**        | **Azure CLI / PowerShell**          | Ferramenta        | Ferramentas de linha de comandos para gestão e automação (cross-platform / Windows).           |
| **Gestão**        | **Azure Cloud Shell**               | Ferramenta        | Terminal acessível via browser (bash ou PowerShell) sem instalação local.                      |
| **Gestão**        | **Azure Arc**                       | Ferramenta        | Permite gerir recursos fora do Azure (on-premises ou outra cloud) através do Azure.            |
| **Gestão**        | **Azure Advisor**                   | Ferramenta        | Analisa configurações e dá recomendações (Custo, Segurança, Performance).                      |
| **Segurança**     | [[Microsoft Entra ID]]              | SaaS              | Serviço de gestão de identidade e acesso (antigo Azure AD).                                    |
| **Segurança**     | **Azure Key Vault**                 | PaaS              | Cofre seguro para guardar segredos, chaves de encriptação e certificados.                      |
| **Segurança**     | **Microsoft Sentinel**              | SaaS              | Solução de SIEM (Security Information and Event Management) e SOAR nativa da nuvem.            |
| **Segurança**     | **DDoS Protection**                 | Serviço           | Proteção contra ataques de negação de serviço distribuído (Basic e Standard).                  |
| **Governação**    | **Azure Policy**                    | Ferramenta        | Define e impõe regras/padrões nos recursos (ex: proibir VMs caras).                            |
| **Governação**    | **Azure Blueprints**                | Ferramenta        | Define um pacote repetível de recursos e políticas (ambiente "carimbado").                     |
| **Custos**        | **Cost Management**                 | Ferramenta        | Monitoriza gastos e define orçamentos com alertas.                                             |
## Funcionamento


## Comparação
* **Concorrentes:** Principal rival da AWS (Amazon) e Google Cloud (GCP).
