---
created: 2026-02-09 11:29
updated: 2026-02-13 15:36
type: concept
status: 🌿
area: Tech
tags:
sources: []
related:
  - "[[Escalabilidade em Nuvem|Escalabilidade]]"
  - "[[Alta Disponibilidade]]"
  - "[[Elasticidade em Nuvem|Elasticidade]]"
aliases:
  - Recursos de Nuvem
  - Cloud Resources
  - Recurso de Nuvem
---

## Definição
**Cloud Computing Resources** são componentes de TI (processamento, armazenamento, rede e inteligência) entregues sob demanda via internet, abstraindo a gestão física do hardware, ou seja, independente da plataforma, os recursos são categorizados pela sua função lógica na arquitetura de sistemas.

## Funcionamento
Os recursos de nuvem funcionam através de camadas de virtualização que dividem grandes hardwares físicos em unidades lógicas menores e isoladas:
1.  **Compute (Computação):** Ciclos de CPU e memória RAM para executar aplicações (ex: Máquinas Virtuais, Contêineres, Funções [[Serverless Computing|Serverless]]).
2.  **Storage (Armazenamento):** Espaço para guardar dados de forma persistente (ex: Object Storage, Block Storage, File Systems).
3.  **Networking (Rede):** Conectividade e segurança (ex: VPCs, Load Balancers, CDNs).
4.  **Database (Dados):** Motores de banco de dados gerenciados (SQL ou NoSQL).

O modelo econômico predominante é o [[Pay-as-you-go]] (pague pelo que usar).

## Comparação
| Critério             | Recursos de Nuvem                         | [[Infraestrutura Tradicional\|On-Premises]] (Local) |
| :------------------- | :---------------------------------------- | :-------------------------------------------------- |
| **Aquisição**        | [[OpEx]] (Despesa Operacional).           | [[CapEx]] (Investimento de Capital).                |
| **Escalabilidade**   | Elástica (Sobe e desce em minutos).       | Rígida (Exige compra e instalação física).          |
| **Responsabilidade** | Compartilhada (Provedor cuida do físico). | Total (Energia, refrigeração, hardware).            |
| **Acesso**           | Remoto/Global via API e Console.          | Físico ou via VPN local.                            |
| **Provisionamento**  | Instantâneo (via código/clique).          | Lento (Logística de compra e setup).                |
