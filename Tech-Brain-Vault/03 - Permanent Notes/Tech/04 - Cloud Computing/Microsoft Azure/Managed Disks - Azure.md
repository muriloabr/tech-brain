---
created: 2026-02-03 14:29
updated: 2026-02-13 15:39
type: concept
status: 🌱
area: Tech
tags:
sources: []
related:
  - Azure Virtual Machine
---

## Definição
Volumes de armazenamento em nível de bloco gerenciados pelo Azure e usados com as [[Virtual Machines - Azure]]. São como "HDs virtuais" plugados na VM.

## Funcionamento
Você escolhe o tamanho e o tipo (HDD, SSD Standard, SSD Premium) e o Azure cuida da infraestrutura física para garantir alta disponibilidade (99.999%).

## Comparação
* **Gerenciado vs Não Gerenciado:** Antigamente, você precisava criar uma "Storage Account" para guardar os discos (complexo). Com o Azure Managed Disk, isso é automático e transparente.
