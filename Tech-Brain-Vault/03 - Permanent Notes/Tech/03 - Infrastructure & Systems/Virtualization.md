---
created: 2026-02-13 16:26
updated: 2026-02-13 16:28
type: concept
status: 🌳
area: Tech
tags: []
sources: []
related:
  - "[[Server]]"
  - "[[Hardware]]"
aliases:
  - Virtualização
  - Server Virtualization
---

## Definição
**Virtualização** é a tecnologia que utiliza software para criar uma camada de abstração sobre o hardware físico, permitindo a criação de múltiplos sistemas computacionais virtuais ([[Máquina Virtual|Máquinas Virtuais]] - VMs) em uma única infraestrutura física. Ela desacopla o sistema operacional da máquina física subjacente, maximizando a utilização de recursos e a flexibilidade de provisionamento.

## Funcionamento
O componente chave é o **Hypervisor** (Monitor de Máquina Virtual), que intercepta comandos do SO convidado (Guest OS) e os traduz para o hardware físico.

Existem duas abordagens arquiteturais principais para o [[Hypervisor]]:
-   **Particionamento de Recursos:** O [[Hypervisor]] divide logicamente [[CPU]], RAM e Disco, garantindo que uma [[Máquina Virtual|VM]] não consuma recursos reservados para outra.
-   **Isolamento de Falhas:** Como cada VM é encapsulada em um arquivo de software, falhas de software ou segurança em uma [[Máquina Virtual|VM]] não afetam o host ou outras [[Máquina Virtual|VMs]].
-   **Encapsulamento:** O estado completo da máquina (BIOS, disco, memória) pode ser salvo em arquivos, permitindo migração (vMotion/Live Migration) e snapshots instantâneos.

## Comparação
| Tipo de Hypervisor | Tipo 1 (Bare Metal / Nativo) | Tipo 2 (Hosted / Hospedeiro) |
| :--- | :--- | :--- |
| **Instalação** | Diretamente sobre o hardware (sem SO prévio). | Instalado como um software sobre um SO convencional (Windows/Linux). |
| **Acesso ao Hardware** | Direto (Alta eficiência e baixa latência). | Indireto (Passa pelo SO hospedeiro antes de chegar ao hardware). |
| **Uso Principal** | Data Centers, Servidores Enterprise, Cloud. | Ambientes de Teste, Desenvolvimento local, Desktops. |
| **Exemplos** | VMware ESXi, Microsoft Hyper-V, KVM, Xen. | Oracle VirtualBox, VMware Workstation, Parallels. |
