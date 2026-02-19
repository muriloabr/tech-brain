---
created: 2026-02-13 15:46
updated: 2026-02-13 16:20
type: concept
status: 🌳
area: Tech
tags: []
sources:
related: []
aliases:
  - Contêineres
  - Containerização
  - Container Engine
---

## Definição
**Container** é uma unidade padrão de software que empacota o código e todas as suas dependências (bibliotecas, configurações, binários) para que a aplicação execute de forma rápida e confiável em qualquer ambiente computacional.

Diferente das [[Máquina Virtual|VMs]], **containers** não emulam hardware; eles virtualizam o Sistema Operacional, compartilhando o mesmo [[Kernel]] do host, mas mantendo processos isolados no nível do usuário ([[User Space]]).

## Funcionamento
A tecnologia de **containers** baseia-se nativamente em funcionalidades do Kernel Linux (embora existam no Windows também):
- **Namespaces:** Garantem o isolamento de visão. O **container** "acha" que tem seu próprio sistema de arquivos, rede e árvore de processos, sem enxergar os do host ou de outros containers.
- **Cgroups (Control Groups):** Garantem o isolamento de recursos. Limitam quanto de [[CPU]] e Memória o **container** pode usar, impedindo que um processo consuma toda a máquina.
- **Union File System:** Permite a criação de camadas (layers) leves e sobrepostas, tornando o armazenamento eficiente.

## Comparação
Para entender containers, é vital não confundir o objeto estático (Imagem) com o objeto em execução (Container).

| Característica   | Imagem (Image)              | Container                               |
| :--------------- | :-------------------------- | :-------------------------------------- |
| **Analogia POO** | A Classe (molde).           | O Objeto (instância).                   |
| **Estado**       | Imutável (Read-only).       | Mutável (Read-write camada superior).   |
| **Função**       | Armazenamento e transporte. | Execução da aplicação.                  |
| **Persistência** | Existe mesmo sem rodar.     | Dura enquanto o processo estiver ativo. |